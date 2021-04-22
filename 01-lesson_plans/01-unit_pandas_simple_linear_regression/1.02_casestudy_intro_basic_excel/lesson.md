# Lesson 1.2: Intro to Excel & Case Study

### Lesson Duration: 3 hours

> Purpose: The purpose of this lesson is to explain one of the business case studies that we will focus on during this cohort and understand the data analysis methodology to solve various business problems through data-driven decision making.

> We will also take a look into git and GitHub that is used as a collaboration tool used heavily in the tech industry.

---

### Setup

> Note: Please make sure that the students have the tool mentioned below set up before you start the lecture. We will only MS Excel in this session. If there is any student that has not installed anaconda yet, please ask the student to take help from the TA at the end of class.

- MS Excel/numbers for Mac/Google Spreadsheets
- Anaconda for Jupyter

---

### Learning Objectives

After this lesson the students will be able to:

- Think like a data analyst. Understand the business case scenario and the business challenges, conduct due diligence, and come up with strategies to solve the questions.
- Perform elementary data pre-processing.
- Merge and blend data from multiple sources using pandas in Python and MS Excel.
- Use Git and Github - or other Git provider - as a collaboration tool.

---

### Lesson 1 key concepts

> :clock10: 20 min

- Briefing about the case study (refer to the files `files_for_lessons/case_study.md` and `files_for_lessons/tasks_lesson_1.md`)

- The description of each variable is provided in `files_for_lessons/variables_description.md`.

In this lesson the task of the instructor is:

* Introduce the "HealthCare for All" business case to the students briefly 
* Show a "high level" overview of the data analytics process
* Show the students how to put in practice some of those data analytics process steps using MS Excel
(Code along with the students)

The steps to follow are:

- Explain the business case scenario that you can find on `files_for_lessons/case_study.md` to the students.  

- Explain the steps to conduc on a data analysis process on a very high level (don't go over the details):

  1. **Define the objective**: optimize the benefits that "Healthcare for All" obtains through mail donations by "Lapsed" donors.
  2. **Gather the data**: data has been already extracted and it's stored in 4 files. We'll just have to consolidate the files.
  3. **Clean the data**: a quick glimpse at `file1` reveals that there are some empty cells, some weird entries (ex: look at column `IC5`). Gender encoding will need some fixing and probably we'll find more obstacles in the way!
  4. **Explore**: here we'll want to answer questions like - how many donors do we have (by gender, by state...) and what's the distribution of their donations for each one of the sub-groups we can find? Are there noticeable differences we can find? We'll try and visualize everything and allow ourselves to be "surprised" by the data beyond the questions we can come up with.
  5. **Process**: Here we'll start looking at what model we want to apply, and we might need to change how some columns are expressed. For example, the "state" and "gender" columns are not numbers, pretty difficult to put them into mathematical equations, right? We'll have to fix that.
  6. **Apply model**: we will create a model to predict the donation each person sends.
  7. **Validate**: we will know if our model is accurate by checking the predictions against a little subset of the data that we'll have previously left out.
  8. **Present**: for this initial project, we won't have to present it.

- In this session, the data is provided in multiple files available in this `files_for_lessons/` folder, namely:
  * file1.xlsx
  * file2.xlsx
  * file3.xlsx
  * vlookup_table.csv

- Show the students what the original data looks like and how the data looks like in the files provided.

- Open the file `files_for_lessons/tasks_lesson_1.md` and show the students how to conduct the steps inside the file, ie:

  1. open a new Excel workbook
  2. select Data->Get Data->From a file->From a workbook from the menu and select file1.xlsx
  3. on the pop up window select "Sheet1" and load data(you can delete the last empty columnns)
  4. go to a new sheet
  5. repeat the steps 1-3 with file2.xlsx, file3.xlsx and file4.xlsx
  6. open a new Excel worksheet and import the file vlookup_table.csv selecting Data->Import data from csv in the menu
  7. concatenate the content of files file1, file2, file3 in a new sheet (named "All" from now on)
  8. on the vlookup sheet, move the column "CONTROLN" to the left most
  9. use Excel "vlookup" function to add the missing columns from vlookup_table.csv to "All" sheet using the "CONTROLN" donnor ID to make the match
  10. use "DOB" (Date of birth) column to find out the age of the donnor. The format of this column is YYMM ( in fact the years are 19YY ;) ). Rember that the reference date if 9706 to compute ages
  11. split the column "DOMAIN" in two in order to find out the type neighborhood they live in (C->"City",T->"Town",R->"Rural",S->"Suburban","U"->"Urban"). Ignore the number for now.
  12. Fix the "IC5" column
  13. Fix the "GENDER" column
  14. Fix the "STATE" columns

:exclamation: Note for instructor: In this Unit, we will take a look at a much simpler version of the case study. We will work only on a sample subset of the data and not on the complete dataset, which has 483 columns and over 98,000 rows.

---

:coffee: **BREAK**

---

### :pencil2: Check for understanding/ Student Activity

> :clock10: 15 min

<details>
  <summary> Click for Instructions: Activity 1 </summary>

(_Share the following link with your students. Students should clone/download repository to be able to work on the tasks._)

- Link to [activity 1](https://github.com/ironhack-edu/data_1.02_excel_activity/blob/master/1.02_activity_1.md).


</details>

---

:coffee: **BREAK**

---

### Lesson 2 key concepts

> :clock10: 20 min

- Gather data from different sources using MS Excel
- Understanding primitive data types: integers, floating-point, characters, strings, and boolean
- Introduction to the data cleaning process

      - Pareto _80-20_ rule for data analysts
      - "Garbage in, garbage out"

- Data wrangling/cleaning process using MS Excel:

      - Standardizing header names
      - Deleting and rearranging columns
      - Working with data types
      - Filtering data
      - Removing duplicates
      - Correcting typos
      - Conditional Formatting
      - Replacing null values

- Use MS Excel with the resulting file from the previous lesson to show the students how to:

  * Remove duplicates
  * Correct typos on "HV1" column
  * Replace numeric missing values with the mean in columns "HV1", "IC1","IC4"

---

:coffee: **BREAK**

---

### :pencil2: Check for understanding/ Student Activity

> :clock10: 15 min

<details>
  <summary> Click for Instructions: Activity 2 </summary>

(_Share the following link with your students. Students should clone/download repository to be able to work on the tasks._)

- Link to [activity 2](https://github.com/ironhack-edu/data_1.02_excel_activity/blob/master/1.02_activity_2.md).

</details>

### Lesson 3 key concepts

> :clock10: 20 min

More about data wrangling/cleaning using MS Excel:

- String functions
- Standardizing data
- `ImportRange` and `indirect` (use the same data with spreadsheets)
- Using `V lookups`/`H lookups`
- Limitations of using MS Excel - A discussion of various other operations we might need to perform

### :pencil2: Check for understanding/ Student Activity

> :clock10: 15 min

<details>
  <summary> Click for Instructions: Activity 3 </summary>

(_Share the following link with your students. Students have already cloned/downloaded repository in the previous activity._)

- Link to [activity 3](https://github.com/ironhack-edu/data_1.02_excel_activity/blob/master/1.02_activity_3.md).

</details>

### Lesson 4 key concepts

> :clock10: 20 min

- Introduction to version control systems

      - Why we need Git and GitHub
      - Configuring git

- Creating a user account on GitHub
- Managing a repository on GitHub

      - Create a repo on GitHub
      - Forking and cloning a repo
      - Make changes and commit to a repo
      - Create a pull request

<details>
  <summary> Click for Sample shell commands </summary>

```shell
$ git	        # displays a list of basic commands with details

# Configuring git
git config --global user.name "<your name>"
git config --global user.email <your_email_address>
git config --list
```

#### Working on GitHub

- Create a new repo on GitHub and then create a repo on the local machine.

```shell
$ mkdir my-repo                 # create an empty folder
$ cd my-repo                    # navigate into it
$ git init 	                    # to initialize an empty git repository
$ touch file.txt                # create an empty file
$ git remote -v                 # to check the remote
$ git remote add origin <link>  # link is the link to the repo on GitHub
$ git remote -v                 # to check if it is added properly

$ git status
$ git add <file name>           # if we just want to add a specific file to the staging area
# Or
$ git add . 		                # if we want to stage to add all the changes made to all the files
$ git commit -m “<message>”
$ git push origin master
```

- Explain what does it mean to clone a repo and demo how to clone.
- Explain what is forking and how to fork
- Explain what does it mean to create a pull request (no need to go into solving conflicts, this will be explained later this week)

</details>

### :pencil2: Practice on key concepts - Lab

> :clock10: 30 min

<details>
  <summary> Click for Instructions: Lab </summary>

- Link to the lab: [https://github.com/ironhack-labs/lab-git](https://github.com/ironhack-labs/lab-git)

</details>
