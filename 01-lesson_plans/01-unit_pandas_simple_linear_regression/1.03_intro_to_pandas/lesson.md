# Lesson 1.3: Intro to Pandas

### Lesson Duration: 3 hours

> Purpose: The purpose of this lesson is to understand the different types of data that we come across as analysts. The students will learn conducting similar data wrangling operations that were implemented in MS Excel including reading data into Python, blending data, working with columns, filtering, and subsetting operations.

---

### Learning Objectives

- Merge or blend data from multiple sources using Pandas in Python
- Work with NumPy and Pandas, both Python essential libraries for data analysis.
- Perform basic data pre-processing operations on dataframes.

> :exclamation: Important note: It is important to emphasize that having sharp business acumen is a very important skill for data analysts.
> An analyst should have good knowledge about the business function that they are helping with the analysis, asking the right set of questions to the clients/stakeholders involved, understanding what are the factors that are driving the business. It is also critical to understand the limitations of the analysis based on the availability of data, do we have the right data to answer the questions that we are trying to solve or would we need more data, and if yes, data on what parameters would we need.

### Lesson 1 key concepts

> :clock10: 20 min

Features and labels, data types in data analysis

- Numerical data
- Categorical data (nominal, ordinal)
- Text data for NLP
- Media data - image, video, voice/speech

<details>
  <summary> Engagement strategies for using pandas library, reading files and data blending </summary>

:exclamation: This might be the first time the students will use a Python library.

> Give an introduction to the library, aliasing, keywords, methods available.
> Open the files using a text editor and show the students how the files are stored based on the file extensions. Ex. the difference between files such as `CSV`, tab-separated values, pipe separated values, etc.
> We are using 4 files in this lesson. Show the students how to use `concat` with 2 files (as you will see in the following Code Sample, you can use `file1.csv` and `file2.txt`), and ask them to read and `concat` the other two files themselves as hands-on practice.
> At this stage it is important to move slowly as the students would be fairly new to using Python libraries. Emphasize the importance to go through the documentation for different functions, etc. At different stages, it is also important to emphasize that the students should play around with the code and analyze the changes in the output.

</details>

- Reading data into Jupyter and data cleaning operations in Python using pandas and NumPy:
  - Introduction to pandas
  - Reading flat files and data blending
  - Standardizing, renaming headers

<details>

<summary> Click for Code Sample Link </summary>

```python
import pandas as pd  # explain keywords are highlighted in green, other strings in red, etc.
import numpy as np

# Reading data
file1 = pd.read_csv('file1.csv')
file1.head()
file2 = pd.read_csv('file2.txt', sep = '\t')  # Show them to read and concat 2 files , other two will be done by students
```

</details>

<details>
<summary> Click for Code Sample Link </summary>

```python
# Data blending
column_names = file1.columns
data = pd.DataFrame(columns=column_names)
data = pd.concat([data,file1, file2], axis=0)
data.shape
```

![Diagram for concatenation](https://education-team-2020.s3-eu-west-1.amazonaws.com/data-analytics/1.3+-+Axes+Explain+-+Data.jpg)

</details>

<details>
<summary> Click for Code Sample Link </summary>

```python
# Standardizing header names
cols = []
for i in range(len(data.columns)):
    cols.append(data.columns[i].lower())
data.columns = cols

# renaming columns
data = data.rename(columns={ 'controln':'id','hv1':'median_home_val', 'ic1':'median_household_income'})
```

</details>

---

:coffee: **BREAK**

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 15 min (+ 5 min Review)

<details>
  <summary> Click for Instructions: Activity 1 </summary>

(_Share the following link with your students. Students should clone/download repository to be able to work on the tasks._)

- Link to [activity 1](https://github.com/ironhack-edu/data_1.03_activities/blob/master/1.03_activity_1.md).

</details>

<details>
  <summary>Click for Solution: Activity 1 solutions</summary>

- Link to [activity 1 solution](https://gist.github.com/ironhack-edu/f013f815c131b186bdcb8ab4f7950ad7).

</details>

---

:coffee: **BREAK**

---

### Lesson 2 key concepts

> :clock10: 20 min

Data wrangling/cleaning using Python:

- Deleting columns
- Rearranging columns
- Filtering and subsetting

<details>
<summary> Click for Code Sample Link </summary>

```python
# deleting columns
data = data.drop(['tcode'], axis =1) # Explain the argument axis, when axis is 0 and 1

# Rearranging columns
data = data[['id', 'state', 'gender', 'median_home_val', 'median_household_income', 'ic2', 'ic3', 'ic4', 'ic5', 'avggift', 'domain', 'dob', 'target_d']]
```

```python
# filtering and subsetting -- using conditions with DataFrame
data[data['gender']=='M']
data[data['gender'].isin(['M', 'F'])]
data[(data['gender']=='M') | (data['gender']=='F')]
data[data['target_d']>100]
```

</details>

---

:coffee: **BREAK**

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 15 min (+ 5 min Review)

<details>
  <summary> Click for Instructions: Activity 2 </summary>

(_Share the following link with your students. Students have already cloned/downloaded repository in the previous activity._)

- Link to [activity 2](https://github.com/ironhack-edu/data_1.03_activities/blob/master/1.03_activity_2.md).

</details>

<details>
  <summary>Click for Solution: Activity 2 solutions</summary>

- Link to [activity 2 solution](https://gist.github.com/ironhack-edu/f34db262b1783abdd78bf7b137c94920).

</details>

---

:coffee: **BREAK**

---

### Lesson 3 key concepts

> :clock10: 20 min

More data wrangling/cleaning with Python:

- Reset index
- Working with indexes

<details>
<summary> Click for Code Sample </summary>

```python
#filter and reset the index

# In this section again emphasize on the importance of playing with the code and checking the output

filtered = data[data['gender']=='M']  # Lets say that we are working on this filtered data
# filtered
filtered = filtered.reset_index(drop=True)
# temp = filtered.copy()
# temp.set_index('state') # This is a dummy case, but indexes should be unique and not nulls, usually auto-increments by 1
```

```python
# Working with indexes
filtered[1:4]
filtered[['gender', 'ic2', 'ic3']][0:10]
filtered.loc[1:3]
filtered.loc[100]
filtered.iloc[1:3]

# now, working just on the indexes row,columns
filtered.iloc[1:10,0:4]
filtered.iloc[[1,2,3,4],[0,2,4]]
```

</details>

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 10 min (+ 5 min Review)

<details>
  <summary> Click for Instructions: Activity 3 </summary>
  
(_Share the following link with your students. Students have already cloned/downloaded repository in the previous activity._)

- Link to [activity 3](https://github.com/ironhack-edu/data_1.03_activities/blob/master/1.03_activity_3.md).

</details>

<details>
  <summary>Click for Solution: Activity 3 solutions</summary>

- Link to [activity 3 solution](https://gist.github.com/ironhack-edu/c724a07ee09037c5ef184dcba2c2fc9e).

</details>

---

:coffee: **BREAK**

---

### Lesson 4 key concepts

> :clock10: 20 min

Data cleaning operations with Python

- Correcting data types
- Removing duplicates

<details>
<summary> Click for Code Sample </summary>

```python
# data types
data.dtypes
data._get_numeric_data()
data._get_bool_data()
data.select_dtypes('object')
```

```python
# correcting data types
data['median_home_val'] =  pd.to_numeric(data['median_home_val'], errors='coerce')
data['ic5'] =  pd.to_numeric(data['ic5'], errors='coerce')
# data._get_numeric_data() # to check if 'median_home_val' and 'ic5' are now listed as numeric data
```

```python
# Removing duplicates
data = data.drop_duplicates()  # play around with the code, show them how to use keep argument
# temp = temp.drop_duplicates(subset=['state','gender', 'ic2', 'ic3'])
# if we want to remove duplicates based on some specific columns
```

</details>

---

:coffee: **BREAK**

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 10 min (+ 5 min Review)

<details>
  <summary> Click for Instructions: Activity 4 </summary>
  
(_Share the following link with your students. Students have already cloned/downloaded repository in the previous activity._)

- Link to [activity 4](https://github.com/ironhack-edu/data_1.03_activities/blob/master/1.03_activity_4.md).

</details>

<details>
  <summary>Click for Solution: Activity 4 solutions</summary>

- Link to [activity 4 solution](https://gist.github.com/ironhack-edu/54fbb3c5299fd77cca9834d93d5dafc3).

</details>

### :pencil2: Practice on key concepts - Lab

> :clock10: 45 min

<details>
  <summary> Click for Instructions: Lab </summary>

- Link to the lab: [https://github.com/ironhack-labs/lab-customer-analysis-round-1](https://github.com/ironhack-labs/lab-customer-analysis-round-1)

</details>

<details>
  <summary> Click for Solution: Lab solutions </summary>

- Link to the [lab solution](https://gist.github.com/ironhack-edu/610b1b0b8a6ab561fdd58faaa2e676d4).

</details>

---

### Additional Resources

- [String functions - documentation](https://docs.python.org/2.5/lib/string-methods.html)
