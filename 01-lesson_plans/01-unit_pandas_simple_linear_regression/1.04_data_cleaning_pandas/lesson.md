# Lesson 1.4: Data Cleaning - Pandas

### Lesson Duration: 3 hours

> Purpose: The purpose of this lesson is to make students familiar with other data cleaning processes including working with null values in numerical and categorical columns, use lambda expression and map functions, and work with DateTime format.

---

### Setup

To start this lesson, students should have:

- Completed lesson 1.3
- All previous Setup

### Learning Objectives

After this lesson, students will be able to:

- Use different methods for replacing null values
- Create user-defined functions for cleaning numerical and categorical columns
- Create anonymous functions/lambda expressions and use them with map functions
- Work with DateTime format and string functions

---

### Lesson 1 key concepts

> :clock10: 20 min

Handling null values in the dataframe

- Removing columns with many null values (threshold based)
- Replacing/imputing null values (numerical)

<details>
<summary> Click for Code Sample </summary>

> :exclamation: Note to the instructor: We will keep working on the same data sets from 1.03 so you can use the same notebook, or use the code below that is commented out to load the data into a new notebook.

```python
# in case of new notebook, use the commented code to load the data:

#import pandas as pd

#file1 = pd.read_csv('../1.03_intro_to_pandas/file1.csv')
#file2 = pd.read_csv('../1.03_intro_to_pandas/file2.txt', sep = '\\t')
#file3 = pd.read_excel('../1.03_intro_to_pandas/file3.xlsx', engine='openpyxl')
#file4 = pd.read_excel('../1.03_intro_to_pandas/file4.xlsx', engine='openpyxl')
#column_names = file1.columns
#donors = pd.DataFrame(columns=column_names)
#donors = pd.concat([file1,file2,file3, file4], axis=0)
#cols = []
#for colname in donors.columns:
#    cols.append(colname.lower())
#donors.columns = cols
#donors = donors.rename(columns={'controln':'id',
#                                'hv1':'median_home_val',
#                                'ic1':'median_household_income'})
#donors['median_home_val'] =  pd.to_numeric(donors['median_home_val'], errors='coerce')
#donors['ic5'] =  pd.to_numeric(donors['ic5'], errors='coerce')
#donors = donors.drop_duplicates()

#donors.shape
    
round(data.isna().sum()/len(data),4)*100  # shows the percentage of null values in a column
nulls_df = pd.DataFrame(round(data.isna().sum()/len(data),4)*100)
nulls_df
nulls_df = nulls_df.reset_index()
nulls_df
nulls_df.columns = ['header_name', 'percent_nulls']
nulls_df
```

- Since there were not many null values in the dataframe, we are taking a dummy value of 3 to show the students how to remove columns with the percentage of null values that are more than a threshold.
- This is usually 60, 70% but it is very case-specific. There is no standard rule and it varies based on the analysts' decisions for that analysis.

```python
columns_drop = nulls_df[nulls_df['percent_nulls']>3]['header_name']  # dummy case with 3
print(columns_drop.values)
# data = data.drop(columns_drop, axis=1)  # drop a list of columns
# data = data.drop(['gender'], axis=1)  # drop a single column
```

```python
# Replacing/imputing null values
data[data['gender'].isna()==True] # checking rows that are null based on a specific column
data = data[data['ic2'].isna()==False] # Since these nulls are not a lot, we can filter them
data

# import numpy
import numpy as np
mean_median_home_value = np.mean(data['median_home_val'])
data['median_home_val'] = data['median_home_val'].fillna(mean_median_home_value)
```

</details>

---

:coffee: **BREAK**

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 10 min (+ 10 min Review)

<details>
  <summary> Click for Instructions: Activity 1 </summary>

(_Share the following link with your students. Students should clone/download repository to be able to work on the tasks._)

- Link to [activity 1](https://github.com/ironhack-edu/data_1.04_activities/blob/master/1.04_activity_1.md).

</details>

<details>
  <summary>Click for Solution: Activity 1 solutions</summary>

- Link to [activity 1 solution](https://gist.github.com/ironhack-edu/b6e092eaf2094895ac9a88340ff82896).

</details>

---

:coffee: **BREAK**

---

### Lesson 2 key concepts

> :clock10: 20 min

- Handling null values in the dataframe

      - Replacing/imputing null values (categorical)

- Lambda expressions

<details>
<summary> Click for Code Sample </summary>

```python
# Replacing null values for categorical variables
data['gender'].value_counts()
len(data[data['gender'].isna()==True])  # number of missing values
data['gender'] = data['gender'].fillna('F')
len(data[data['gender'].isna()==True]) # now this number is 0

# Exporting this processed data to a csv
data.to_csv('merged_clean_ver1.csv') # you can find this file inside files_for_lesson_and_activities folder
```

> :exclamation: Note to the instructor: It is important to emphasize on documenting your work and saving copies of data. For now, documentation can be done simply by adding more comment sections in their codes. Saving copies of data is also important so that you don't have to repeat/re-run the code every time from the beginning since we are using many operations from multiple lessons.

</details>

<details>
<summary> Click for Code Sample </summary>

```python
# lambda expressions
y = lambda x: x+2
print(y(2))

square = lambda x: x*x
square(4)

addition = lambda x,y : x+y
addition(1,3)

lst = [1,2,3,4,5,6,7,8,10]
new_list = []
for item in lst:
    new_list.append(square(item))
new_list

new_list = [square(item) for item in lst] # list comprehension
new_list

new_list = [square(item) for item in lst if item%2==0]
```

</details>

---

:coffee: **BREAK**

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 10 min (+ 10 min Review)

<details>
  <summary> Click for Instructions: Activity 2 </summary>

(_Share the following link with your students. Students have already cloned/downloaded repository in the previous activity._)

- Link to [activity 2](https://github.com/ironhack-edu/data_1.04_activities/blob/master/1.04_activity_2.md).

</details>

<details>
  <summary>Click for Solution: Activity 2 solutions</summary>

- Link to [activity 2 solution](https://gist.github.com/ironhack-edu/287b1ed5d542d7de2a23558835560f08).

</details>

### Lesson 3 key concepts

> :clock10: 20 min

- Map functions

      - Map functions and lambda expressions for data cleaning

- Define a custom function to clean categorical columns

```python
# map functions
data.columns = list(map(lambda x: x.lower(), data.columns))
data['gender'].unique() # check the unique values in the column
data['gender'] = list(map(lambda x: x.upper(), data['gender']))
```

```python
data['gender'].unique()  # check the unique elements in the column
# Now define a function to clean the column
def clean(x):
    if x in ['M', 'MALE']:
        return 'Male'
    elif x.startswith('F'):
        return 'Female'
    else:
        return 'U'
data['gender'] = list(map(clean, data['gender']))
data['gender'].unique()  # To check the results again

# define another method to clean the column "state" in the dataframe. This can be an activity
```

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 10 min (+ 10 min Review)

<details>
  <summary> Click for Instructions: Activity 3 </summary>

(_Share the following link with your students. Students have already cloned/downloaded repository in the previous activity._)

- Link to [activity 3](https://github.com/ironhack-edu/data_1.04_activities/blob/master/1.04_activity_3.md).

</details>

<details>
  <summary>Click for Solution: Activity 3 solutions</summary>

- Link to [activity 3 solution](https://gist.github.com/ironhack-edu/f57c649de9930d7a4efc0af0e99f3044).

</details>

---

:coffee: **BREAK**

---

### Lesson 4 key concepts

> :clock10: 20 min

More data wrangling/cleaning using Python:

- Working with DateTime format
- Using string functions

<details>
<summary> Click for Code Sample </summary>

```python
# Examples of working with datetime format:

file = pd.read_csv('df_final_web_data_pt_1.csv')
file.dtypes

file['date_time'] = pd.to_datetime(file['date_time'], errors='coerce')
file['date_time'][0].day
file['date_time'][0].month
file['date_time'][0].year
file['date_time'][0].isoweekday()  # Returns 1 for Monday and so on

file['date_time'][0].time()
file['date_time'][0].isoweekday()
file['date_time'][0].isoformat()
file['date_time'][0].strftime(format='%d-%m-%Y')
file['date_time'][0].strftime(format="%A %d. %B %Y")

import time
from datetime import date

today = date.today()
today

time.localtime(time.time())
time.gmtime(time.time())
```

```python
# Examples of working with string functions

string = " I am learning  data  analysis at Ironhack  . It is  super easy "
string.lower()
string.upper()
'34'.isdigit() # does not work with decimal numbers
string.lstrip()
string.rstrip()
string.split()
string.split('.')
string.replace('  ', '')
```

</details>

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 10 min (+ 10 min Review)

<details>
  <summary> Click for Instructions: Activity 4 </summary>

(_Share the following link with your students. Students have already cloned/downloaded repository in the previous activity._)

- Link to [activity 4](https://github.com/ironhack-edu/data_1.04_activities/blob/master/1.04_activity_4.md).

</details>

<details>
  <summary>Click for Solution: Activity 4 solutions</summary>

- Link to [activity 4 solution](https://gist.github.com/ironhack-edu/128d7bc55113d981393703e03ce98093).

</details>

---

:coffee: **BREAK**

---

### :pencil2: Practice on key concepts - Lab

> :clock10: 30 min

<details>
  <summary> Click for Instructions: Lab </summary>

- Link to the lab: [https://github.com/ironhack-labs/lab-customer-analysis-round-2](https://github.com/ironhack-labs/lab-customer-analysis-round-2)

</details>

<details>
  <summary>Click for Solution: Lab solutions</summary>

- Link to the [lab solution](https://gist.github.com/ironhack-edu/8c59068a9aa24bf9fffcd4cf3eefe453).

</details>

---

### Additional Resources

- [Python DateTime](https://www.programiz.com/python-programming/datetime)
- [Python String Methods](https://www.programiz.com/python-programming/methods/string)
