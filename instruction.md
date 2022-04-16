## 1. install git
`git --version`
<br>

## 2. configure your name & email (in git bash)

```
git config --global user.name "your name"
git config --global user.email "your@email.com"
```
<br>

`ls` - list 

`git init` - it tells me initialised empty git repository

`ls -a` - to view hidden files and folders. there's now a dot git. 

<br>

## checking the status
`git status` - often used when working w git. it shows us which files have been changed, which files are tracked, etc

`touch project.html` - to create new files | such as create `program.cpp`, `hello.html`, etc

`git add file.js` or `git add .` for all files | or `git files.js files.html files.css` for selecting that you wanna added
<br>

## Making commits
`git commit -m "commit message"` - `-m` message | allows you to write description abt what you've done updated
<br>

## check history

`git log` - to give me a history | **note:** you need to add description on `-m`, so that you can see what history. 
<br>

## undo your project

if you wanna undo your project after you changed. and you wanna go back to previous code just like time machine

`git checkout <commit-hash>` 

e.g: `git checkout 836900392f8159bd3260f8a7c9c3dd837a2dcaf3`

<br>

-----------

## braches
branch in git is like a timeline of your application of the repository
<br>

## creating a new branch
`git branch <new-branch-name>`

`git branch` - to check what's your branch you doing right now

---------

## step-by-step how to use `git merge`

here the instruction that if you wanna add extra code, then how to use it. 


`git branch crazycolors` - to add new branch to make your project or add code (on master)

`git branch` - to check again

```
<!-- output:  -->
crazycolors
* master
```
<br>

`git checkout crazycolors` - to switch branch into "crazycolors" that you wanna add code.

after you finish to add extra code on `crazycolors`  (on crazycolors)

`git add .` (on crazycolors)

`git commit -m "add animated bg"` (on crazycolors)

`git log` - to check and see `"add animated bg"` has added on message (on crazycolors)

`git branch` 

```
<!-- output:  -->
*crazycolors
master
```
<br>

`git checkout master` - now switch into "master" (on master)

`git log` - to check again, but not show `"add animated bg"` (on master)

`git branch` to check again, make sure you are on "master"

`git merge crazycolors` - to connect and add your project from `crazycolors` into `master` (on master)

`git log` - to check again | and it now has showed "add animated bg"


## put this code project into github using git

once you've done make project or wanna put this code 

`git remote add origin <put git this link on SSH key>`

`git push -u origin main` - then refresh your browser on github, to check whether files already put in it.

`git push` - if you add smth, or extra code, don't forget `git add` + `git commit -m "yada yada"`, then `git push` to upload your github website. then refresh again on browser and it will pop up the updated that you've added the code.







