![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Contributing

## Table of content

- [How can I contribute?](#how-can-I-contribute?)
  - [Reporting Bugs / Suggesting Enhancements](#reporting-bugs--suggesting-enhancements)
    - [How to create an Issue on GitHub?](#how-to-create-an-issue-on-github)
  - [Pull Requests](#pull-requests)
  - [Your first contribution? Not a problem!](#your-first-contribution-not-a-problem)
    - [What is a contribution?](#what-is-a-contribution)
    - [Who can make a contribution?](#who-can-make-a-contribution)
    - [Before we start - vocabulary](#before-we-start---vocabulary)
    - [What do I have to know in order to make a contribution?](#what-do-i-have-to-know-in-order-to-make-a-contributions)
    - [Naming the branches](#naming-the-branches)
    - [Guided example](#guided-example)

## How can I contribute?

### Reporting Bugs / Suggesting Enhancements

Bugs are tracked as [GitHub issues](https://guides.github.com/features/issues/). Before submitting a new GitHub issue, check if it wasn't created already by going through the already existing [list](https://github.com/ironhack-edu/data-bootcamp/issues).

#### How to create an issue on GitHub?

By creating the issue you’re pointing out that something either needs to be corrected or improved or removed or you’re suggesting some new topics that we should include in our curriculum. (If you are not familiar with this term please check the _Before we start - vocabulary_ section.)

To be able to create an issue, you have to be inside the repository on GitHub. In the navigation bar you can see Issues tab and by clicking on it you can see the list of open issues but also you can open an issue.

> <details>
>   <summary> :person_fencing: Click to see image :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/PWlNNsH.png)
>
> </details>

<br>

When you click on **New Issue**, you will see this window:

![](https://i.imgur.com/S47nuFT.png)

> <details>
>   <summary> :person_fencing: Click here to see an example of an issue :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/ysRytRk.png)
>
> </details>

<hr>

### Pull Requests

- Find an issue that you are interested in addressing. If there is no issue, first open one.
- When you already have cloned repository, create a new branch for your fix (or feature) using:

```shell
$ git checkout -b branch-name
```

This branch will be created from `develop` branch.

- Make the changes for the issue you are trying to address or the feature that you want to add.

- Add and commit changes:

```shell
$ git add .
$ git commit -m"short and descriptive message to explain your work"
```

- Before pushing your changes and making pull request, make sure your local branch is up to date with `ironhack-edu/data-bootcamp/develop` branch:

```shell
$ git pull origin develop
```

Some conflicts might happen here - try to resolve them and in that case, add and commit them again asnd in the end, push all changes:

```shell
$ git push origin branch-name
```

<hr>

### Your first contribution? Not a problem!

#### What is a contribution?

Any change you want to make, whether it’s just **fixing the typo** in the lesson, **updating the code**, or **suggesting a minor or major update to any learning unit** is considered a contribution.
Besides doing Pull Request, you can open **ISSUE** with any suggestion or update you think it should be made. If you don’t have time to make the change yourself, but you noticed something that needs to be fixed (typo, grammar, code bug) please follow the steps in the Issue section. **The main goal is to raise awareness and point the place where the update needs to be made.**

#### Who can make a contribution?

Any member of Ironhack who has access to the **[data-bootcamp](https://github.com/ironhack-edu/data-bootcamp)** repository (folder) in Ironhack GitHub has the power on giving their contributions.

#### Before we start - vocabulary

- [Git](https://brennan.io/2015/08/07/github-noncoders/#:~:text=Git%2C%20for%20Non%2DCoders,without%20messing%20up%20their%20progress.)
- [GitHub](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=GitHub%20101,their%20peers%20are%20working%20on.)
- [Repository](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=Sometimes%20shortened%20to%20just%20%E2%80%9Crepo,file%20folders%20on%20a%20computer.)
- [Branch](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=Each%20repository%20can%20contain%20multiple,the%20primary%20branch%20if%20desired.)
- [Clone](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=A%20copy%20of%20a%20repository%20that%20is%20hosted%20locally)
- [Commit](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=A%20record%20of%20a%20change%20made%20to%20a%20file%20or%20files%20in%20the%20repository)
- [Fork](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=is%20when%20you%20copy%20another%20user%E2%80%99s%20repository%20to%20your%20own%20account)
- [Pull/push](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=Merging%20changes%20made%20to%20the%20repository%20files%20into%20the%20local%20copy)
- [Pull Request (PR)](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=When%20you%20want%20to%20make%20changes%20to%20a%20repository%20you%E2%80%99re%20working%20on%20as%20part%20of%20a%20collaborative%20project,%20you%20send%20a%20%E2%80%9Cpull%20request.%E2%80%9D)
- [Versioning](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=Refers%20to%20recording%20and%20tracking%20the%20revisions%20made%20to%20a%20project)
- [Issues](https://unito.io/blog/guide-to-github-for-project-managers/#:~:text=They%E2%80%99re%20mainly%20used%20to%20track%20bugs,%20but%20they%20can%20also%20be%20used%20to%20collect%20user%20feedback%20and%20organize%20tasks)
- If you are super curious about Remote branches, check out this [freecodecamp page](https://www.freecodecamp.org/news/git-checkout-remote-branch-tutorial/).

#### What do I have to know in order to make a contribution?

You will have to have the **[data-bootcamp](https://github.com/ironhack-edu/data-bootcamp)** repository (folder) locally on your computer. How to do this? (for the first time contributors)

**Steps to follow**:

1. Copy this repo locally. All the changes you make locally you should push upstream to master (we'll cover this later). Also, you should pull changes others make to have them available locally (we'll cover this too later).

   How to do this, you might ask. When you are already on the GitHub repo you want to clone, you should see <span style="background-color: #32CD32; padding: 5px; border-radius: 4px;">**Code**</span> button in the right upper part of the page.

> <details>
>   <summary> :person_fencing: Click here to check the this screen should look like :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/aCvPX8K.png)
>
> </details>

<br>

2. On your laptop, using the CLI, navigate to the place where you would like to save the the folder and follow the next few commands (do not use the `$` sign):

   ```shell
   $ git clone https://github.com/ironhack-edu/data-bootcamp

   $ cd data-bootcamp
   ```

   To check all the files, you should run the `ls` (list) command to see the available folders and files inside the main repo.

> <details>
>   <summary> :person_fencing: Click here to check the this screen should look like (this is the example repo FYI) :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/d9nwIJ2.png)
>
> </details>

<br>

3. When we clone the repository, it automatically creates a **`master`** branch that tracks the **`origin/master`**. After executing the **`git branch`** command, you should see that we have only one branch, and that is the **`master`** branch:

   ```shell
   $ git branch

   # * master
   ```

<br>

4. Now let’s get familiar with the branches we will work with. The _`master`_ branch will be the **untouched source of truth** and it will be the branch that we will base our production on.

   Besides the master branch, for us very important is the **develop** branch. This branch exists on the origin and it is going to be your source of truth since you will be pulling all the changes from the **develop** branch and we will be merging all your updates into **develop** branch primarily.

   So the next step is to create a develop branch locally and set it to track remote develop branch (the one on origin). The best way to do this is by running the command in this format:

```shell
# example
$ git checkout -b [branch] [remoteName]/[branch]
```

Using this is recommended if you want to name your local branch differently than the remote one. However, the best practice is to name them equally so you can use the shorthand provided by git:

```shell
# how you should do it
$ git checkout -b develop
```

_If `develop` branch already exists, proceed to the next step: pull the changes to make sure the branch is up to date._

To pull the changes from the **`develop`** brach, use the following command:

```shell
$ git pull origin develop
```

Now you have all the content on your computer and now let’s go over how you can push some change that you’ve just made in some lesson.

:heavy_exclamation_mark: **RULE 1**: We will never make changes directly on develop branch and push changes into develop branch.

<br>

#### Naming the branches

In order to push an update, you will create a new branch with a very descriptive name; the suggested name would be <span style="background-color: #82E0AA">"yourName-lesson-title" </span>.

:heavy_exclamation_mark: **RULE 2**: Before you make branch and submit changes, check if anyone else did the same already.

<br>

> <details>
>   <summary> :person_fencing: Click here to check existing branches :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/kW9R23W.png)
>
> </details>

If there is already a branch with the name of the lesson you were planning to work on, choose the branch and the latest commit to see what was changed most recently. If you see that the issue you wanted to fix is already fixed, that’s great, you don’t have to do anything. If you find something else that needs to be fixed, open a new branch with your name and lesson title and submit your update.

<br>

#### Guided example

a) You want to update the lesson “Node intro and installation”. You will go ahead and create branch "yourName-node-intro"

> <details>
>   <summary> :person_fencing: Click here to see an example :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/YoxRwzu.png)
>
> </details>

<br>

b) Next thing, you will open the lesson you want to update in the code editor (I’m using VS code, that’s why I start with `code .`. In your case, this might be different, depending on the code editor you use).

> <details>
>   <summary> :person_fencing: Click here to see an example :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/23WTf3i.png)
>
> </details>

<br>

c) After you made changes, you will follow these steps:

```shell
$ git add .
$ git commit -m”describe what you did”
$ git push --set-upstream origin sandra-node-intro
```

In the git _commit_ part you shouldn’t go into details, but just overall what you did. However, when you make pull requests you should describe what exactly did you change in the lesson.

> <details>
>   <summary> :person_fencing: Click here to see an example :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/99Gx54w.png)
>   ![](https://i.imgur.com/JkITwZ4.png)
>
> </details>

<br>

c) Let’s go to the Ironhack GitHub account and make a Pull Request (PR). Go inside the folder you want to make contributions to and make a Pull Request.

> <details>
>   <summary> :person_fencing: Click here to see an example :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/V0tPaRk.png)
>
> </details>

> <details>
>   <summary> :person_fencing: After clicking on Pull Request, you should see the next page (click here) :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/UdMePKg.png)
>
> </details>

<br>

<p style="background-color: #3EE6DE">:information_source: Make sure you add <b>sandrabosk</b> as a Reviewer. </p>

<br/>

> <details>
>   <summary>To summarize, the steps to follow (click to see) </summary>
>
> 1.  make sure you’re on the **right branch** (the one you created locally and just pushed changes from it)
> 2.  You want to make PR to **develop** branch.
> 3.  Explain changes you made.
> 4.  Reviewers: add <span style="background-color: yellow">the curriculum owner and `@sandrabosk` </span> as the Reviewer.
> 5.  Click on Create pull request

> </details>

<br/>

After this point, the Reviewer will get the notification that you made a Pull Request and Reviewer will check it and merge it. In case there’s something Reviewer doesn’t understand, they will contact you prior to merging your PR.

<br>

d) Every next time you want to make any updates/contributions, you very **first step** (that should be done locally in your CLI) is to - **get all the changes locally as well**, that is, you want **your local `develop` branch to be up-to-date with `origin/develop` branch**. In order to make that happen, you have to be on develop branch (to go to develop, run: `git checkout develop`), and afterward run: **`git pull`**.

To summarize:

```shell
$ git checkout develop # to go to your local develop branch

$ git pull # to get the changes from the remote develop to your local develop branch
```

> <details>
>   <summary> :person_fencing: Click here to see an example :person_fencing: </summary>
>    
>   ![](https://i.imgur.com/UhsfMlF.png)
>
> </details>

So now, all the changes you or someone else made, you have locally as well. These are the changes from the branches that are already merged into the `origin/develop` branch. <span style="background-color: #3EE6DE;">You should do this every time you want to update any of the lessons inside CareerHack folder.</span>

<br>

##### What's next?

Reviewer will check your updates, ask for updates if needed and and merge to `develop` once it is ready. Eventually when there is a new release `develop` will be merged into the `master` branch.

<br><br>

<p style="background-color: #4CC4EF; padding: 10px; border-radius: 5px;"> Thank you so much! We can make the curriculum much better in much shorter time if we all work together. ♥️ </p>

<!--
If submitting a new _lesson_ or _lab_ resource, please also make sure you read the following resources:

- Follow ironhack's [styleguide](styleguide.md), so we can keep consistent resources
- Are in the standard [lesson](templates/template-lesson.md) and [lab](templates/template-lab.md) templates -->
