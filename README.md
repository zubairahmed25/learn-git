<img src="https://devmounta.in/img/logowhiteblue.png" width="250" align="right">

# Project Summary

Practice using git + Github

This project will consist of three separate mini-projects to get you comfortable with the kinds of activities you'll be using git for throughout the class. 

In the first mini-project, you'll be mimicking the steps you'll take when you first start your personal project. Creating a repository, linking it to your computer, then pushing those changes up to your GitHub.

In the second mini-project, you'll be mimicking the steps you'll take with nearly every DevMountain project you do. You'll 'fork' the DevMountain repository, link your computer with your fork, then pushing those changes up to your GitHub.

Finally, in the last mini-project you'll be mimicking the steps you'll take during the group project portion. You'll fork your group's repo, link your computer with your fork, push changes to your GitHub, then make a 'Pull Request' into your group's repo.

## Mini-Project 1: Personal Project

## Step 1

### Summary

In this step we will create a repository on GitHUB.

### Instructions

* Go to <a href="https://github.com/">GitHub</a>.
* Sign in to GitHub.
* On the right side of the page, click on the green `New repository` button.
* Give your repository any name you like and make sure that the repository is public.
* Also make sure that the `Initialize this repository with a README` is <b>NOT</b> checked.

## Step 2

### Summary

In this step we will setup the origin for the repository. We'll do this by connecting code on our computer to the GitHub repository we just created.

### Instructions

* Create a folder called `myProject`.
* Go into that folder.
* Create a file called `myName.js` and add your name to that file.
* Save the file and open a terminal window.
* In your terminal window, `cd` to your `myProject` folder. O
* Run `git init`. 
  * <details>

    <summary> What just happened? </summary>

    <br />

    You've just told your computer that you want git to watch the `myProject` folder and to keep track of any changes. This also allows us to run git commands inside of the folder. (Warning:  Be very careful to make sure you're in the right directory when you run `git init`!)

    </details>
* Run `git remote add origin [Repository URL goes here]`. You can get your URL from going to repository you made earlier in your browser and copying the address.
  * <details>

    <summary> What just happened? </summary>

    <br />

    Basically, we tell our computer "Hey, I created this repo on GitHub, so when I push, I want my code to go to this GitHub repo." Now whenever you run `git push origin master` your computer knows that origin is pointing to your repo you made on GitHub and it pushes your changes there.

    <br />

    ( If you accidentally DID initialize your repository with a README, you must do a `git pull origin master` first - to get the README file on your computer - before you'll be able to push. ) 

    </details>

## Step 3: Push your code to GitHub

### Summary

In this step, we will push code to GitHub.

### Instructions

* Open a terminal window and make sure it is in the directory of `myProject`.
* Run `git status`.
  * <details>

    <summary> What does this do? </summary>

    <br />

    This will show what files have been changed. This also helps us determine what files we want to add to GitHub and what files we don't want to add to GitHub.

    </details>
* Run `git diff`.
  * <details>

    <summary> What does this do? </summary>

    <br />

    This will show the actual code that has been changed. Again, we want to make sure we don't push anything to GitHub that shouldn't be there.

    </details>
* Run `git add nameOfMyFile.fileExtension`.
  * <details>

    <summary> What does this do? </summary>

    <br />

    This adds our file(s) to the 'staging area'. This is basically a fail safe if you accidentially add something you don't want. You can view items that our staged by running `git status`.

    </details>
* Run `git commit -m "The sentence I want associated with this commit message"`.
  * <details>

    <summary> What does this do? </summary>

    <br />

    This tells your computer: 'Hey, the next time code is pushed to GitHub, take all of this code with it.' The message also specifies what GitHub will display in relation to this commit.

    </details>
* Run `git push origin master`
  * <details>

    <summary> What does this do? </summary>

    <br />

    Your code is now pushed to GitHub. Be sure to include `origin master`, as this tells GitHub which branch you want to push to, and creates the branch if it doesn't exist yet.

    </details>
* Go to your repository on GitHub and see your updates.

##Mini-Project 2: DevMountain Project
* Now what we're going to do is walk through how you would normally treat a day's project here at DevMountain. 

### Step 1: Fork the Repo
First, you'll want to 'fork' the repo. On the top right of this page, you should see a button that says 'fork.' This will essentially copy all of the code from this repository, but make it as a new repository under your account. As you can imagine, you can't push directly to the DevMountain repo, because that would not be secure for DevMountain (anyone could make any changes they want). What you should do is create a fork of this repo, then push to your own fork because it's under your own account.

### Step 2: Clone the Fork
* Once you've forked this repo, you're going to want to clone your forked repository. Go to your freshly forked page and copy the url (click on the green "clone or download" button on the right). Then, head over to your terminal and type `git clone [Repository URL]`, replacing Repositry URL with the URL you just grabbed from GitHub. This takes what's on GitHub and essentially downloads it so you can now make changes to it on your local computer.
* Once you've cloned your fork, open up your fork in Sublime Text and make a change. Once you've made a change head over to your terminal and type `git status`, you should see that a file has been changed. If you see the file, run through the steps outlined above in Mini-Project 1 (status, diff, add, commit, push). Note that when you run `git push origin master` in this repository, origin is already pointing to your forked repo since you used `git clone`. Unlike the last step, you don't need to tell your computer where to push your code because git already knows.

##Mini-Project 3: Group Project
* We're essentially going to redo all the same steps we did in Mini-Project 2, but add one more step. 

### Step 1: Re-clone Your Fork

Note: to re-clone your fork, you must do one of three things: 
1. Delete the folder on your computer, or
2. Rename the folder on your computer, or
3. Rename the second clone by doing ```git clone [repo url] [new folder name]```
If you do not do one of these three things, when you try to do a git clone, it will give you an error saying it already exists.

* Re-clone your fork of this project to your local computer, make a change, add, commit, then push that change. 

* Go to your forked repo on GitHub and verify your change is there. 

Let's imagine we're working in groups. If we have everyone pushing to one repo without verifying the quality of the code, things can get messy pretty quick. GitHub fixed this solution with 'Pull Requests.' Basically, you fork a project, make changes to your fork, then you make a Pull Request (PR) back into the original project requesting that some piece of code be added to the original repo. This is how the vast majority of open source code projects work.

### Step 2: Make the PR
* Go to your forked repo on github and click where it says 'Pull Request', and click 'New pull request'. It should show you the file changes you've made and how they differ from the original repo. If it does, click on the 'create pull request' button to submit your pull request. 
* Now, I should see your pull request and I can decide if I want to add that code into the main project or not.

## Contributions
If you see a problem or a typo, please fork, make the necessary changes, and create a pull request so we can review your changes and merge them into the master repo and branch.

## Copyright

© DevMountain LLC, 2015. Unauthorized use and/or duplication of this material without express and written permission from DevMountain, LLC is strictly prohibited. Excerpts and links may be used, provided that full and clear credit is given to DevMountain with appropriate and specific direction to the original content.

<img src="https://devmounta.in/img/logowhiteblue.png" width="250">
