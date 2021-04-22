# Lesson 1.9: Improving the model

### Lesson Duration: 3 hours

> Purpose: The purpose of this DIY (Do It Yourself) lesson is to go through the complete process of building the model and using different techniques to improve the accuracy of the model. As George Box famously said, "All models are wrong but some are useful".
> Students will also understand what the git is and how to use GitHub. As a final learning for today, students will realise the importance of delivery and presentation of the analysis/findings from the data analysis journey.

> Important note: We would also also make sure that the students have installed either Sequel Pro or MySQL Workbench by the end of the week, preferably in class on Friday. To check if everything is installed and set up correctly, we will load the database that will be used in class. The sql file is provided in this folder.

> There is another folder with instructions to load SQL data into Sequel Pro. Similar steps could be followed to import sql file in MySQL WOrkbench. Before the end of the day students should have the database ready for the next week.

> In Jupyter, the students should install `sqlalchemy` and `PyMySQL`, which will be used later in the week to connect SQL with python IDE. The `sqlalchemy` is the library/database toolkit for Python for database connections and `PyMySQL` is the driver. We have different drivers based on the type of database we are trying to connect to.

### Learning Objectives

After this lesson, students will be able to:

- Apply a linear regression model from the beginning
- Improve the accuracy of the model
- Collaborate using Git and GitHub
- Deliver impactful presentations

- Install sequelPro/MySQL Workbench (if not installed)
- Load SQL database
- Install `sqlalchemy` and `PyMySQL`

---

### Lesson 1 key concepts

> :clock10: 20 mins

- Revisiting the model
- List down the followed steps
- Spot the areas in the model where changes could be made
- Apply the changes
- Fit the model and check the accuracy
- Compare the changes in the different models

:exclamation: Note for instructor: In this session, discuss with the students the complete process that was followed from data collection, data cleaning, processing, and building the model. Suggest places where changes could be made and ask students to apply those changes and check the accuracy of the model. They can compare different models and select the model that is performing the best. Here, we should also emphasize that, while conducting such analysis, different models are tried and tested and the model that gives the most accurate results is chosen.

Some changes that could be suggested include different data processing techniques such are:

    - Choosing a different way to fill null values
    - Working with a categorical variable to reduce the number of categories
    - Different data transformation
    - A different method of remove outliers
    - Choosing different scaling method

In this lesson, the students will devise the strategy to work on their project. We will ask the students to work on it in the second half of the day, after the lessons on git and GitHub, and the presentations are over.

---

### :pencil2: Practice on key concepts - Lab

> :clock10: 30 min

<details>
  <summary> Click for Instructions: Lab </summary>

- Link to the lab: [https://github.com/ironhack-labs/lab-customer-analysis-round-7](https://github.com/ironhack-labs/lab-customer-analysis-round-7)

</details>

<details>
  <summary>Click for Solution: Lab solutions</summary>

- Link to the [lab solution](https://gist.github.com/ironhack-edu/1a9470475c74ea34e4c9931c642ebece).

</details>

---

### Lesson 2 key concepts

> :clock10: 20 min

- Quick recap to version control systems: Why git and Github?
- Managing a repository on GitHub (quick recap - already discussed on day 1):
  - Create a repo
  - Make changes and commit to a repo
  - Forking and cloning a repo
  - Fork vs. clone
  - Create a pull request

</details>

---

:coffee: **BREAK**

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 10 min (+ 10 min Review)

<details>
  <summary> Click for Instructions: Activity 1 </summary>

- Fist to five

How everyone is doing with git and GitHub?

</details>

---

:coffee: **BREAK**

---

### Lesson 3 key concepts

> :clock10: 20 min

- Working with branches
- Resolving merge conflicts
- Adding large files on GitHub
- Initializing directories on personal computer as GitHub repos

<details>
<summary> Click for Code Sample </summary>

```shell
$ git branch 	                        # shows the current branches in the repo
$ git branch -a 	                    # shows all branches (even the ones you haven't worked on)
$ git checkout -b <NameOfNewBranch>	  # creates new branch
$ git checkout <BranchName> 	        # switches to the branch we want to work on
$ git pull 	                          # pulls the latest changes to the branch we are working on (git pull = git fetch + git merge)
$ git fetch 	                        # gets all branches from the repository
```

# Merging Branches

Case 1: Merges changes in branch to the master file

```shell
$ git checkout master
$ git merge <Name of Branch to be merged to Master>
```

Case 2: Merges changes in master file to the branch

```shell
$ git checkout <branch name>
$ git merge master
```

</details>

---

:coffee: **BREAK**

---

### Lesson 4 key concepts

> :clock10: 20 min

- Presentations/reporting the results of your analysis

  - Create visually appealing presentations
  - Understanding your audience/key stakeholders
  - Demonstrate business acumen/strong business knowledge
  - Creating a story to answer business questions
  - Deliver actionable insights and business insights
  - "Everything should be made as simple as possible, but not simpler"

---

#### :pencil2: Check for Understanding - Class activity/quick quiz

> :clock10: 10 min (+ 10 min Review)

<details>
  <summary> Click for Instructions: Activity 2 </summary>

**Daisy chain**

Check the full analysis process, step by step.

</details>

<details>
  <summary>Click for Solution: Activity 2 solutions</summary>

1. Problem (case study)
2. Getting Data
3. Cleaning/Wrangling/EDA
4. Processing Data
5. Modeling
6. Model Validation
7. Reporting

</details>

---

:coffee: **BREAK**

---

### :pencil2: Practice on key concepts - Lab

> :clock10: 30 min

<details>
  <summary> Click for Instructions: Lab </summary>

- Link to the lab: [https://github.com/ironhack-labs/lab-customer-analysis-final-round](https://github.com/ironhack-labs/lab-customer-analysis-final-round)

</details>

<details>
  <summary>Click for Solution: Lab solutions</summary>

- Link to the [lab solution](https://gist.github.com/ironhack-edu/90b5ce9b3dfd88f1918c2cf1d2dd1dbf).

</details>

---

### Additional Resources

- [Best practices for PowerPoint presentations](https://alum.mit.edu/best-practices-powerpoint-presentations)
- [More tips on PowerPoint formatting](https://www.workfront.com/blog/10-tips-for-designing-presentations-that-dont-suck-part-1)
