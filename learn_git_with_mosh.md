### Youtube: Git Tutorial for Beginners: Learn Git in 1 Hour

### installing git
`git --version` - download the latest version is recommended 

git BASH - the next thing is **git BASH** once you've done download git version

---

### configuring git

**settings**
* Name
* Email
* Default Editor
* Line Ending

**Level**
* system - all users (of the current computer) | top level
* global - All repositories of the current user | global level
* local - The current repository; the repo in the current folder | below level

---
### Name & email
```
git config --global user.name "your name"
git config --global user.email "your@email.com"
```

---
time: 9.46

`git config --global core.editor "code --wait"`

`git config --global -e"`

`git config --global core.autocrlf true"`

---

### getting help

`git config --help` - open browser for more info about command

`git config --h` - for quick summary about command


### initialising a repository
~/projects
`mkdir Moon`

~/projects
`cd Moon`

~/projects/Moon
`git init` - we wanna add this file to a git repository. we have to initialise a new empty.  

after enter `git init` check this output, full path, we have moon directory & inside this directory, we have a sub directory called **dot git** by default.
```
output:
Initialized empty Git repository in /Users/moshfeghhamedani/Projects/Moon/.git/
```

this subdirectory is hidden, because you're not supposed to touch it (`.git/`)

~/projects/Moon > **git 🌿 main**
`ls` - list all the files | but we don't see anything

`ls -a` - but we can type `ls -a` which short for **all** | and we can see the git subdirectory

```
output:
. .. .git
```

`open .git` - to take a look open the file where your path | once you open it, this is where git stores information about our *project history*


### remove git repo
if you wanna remove the git sub directory
~/projects/Moon > **git 🌿 main**
`rm -rf .git`

*~/projects/Moon* - now become this

--- 

### git workflow
`git add files.js` - to update what you've changed, edit, deletion, fix, etc

`git commit -m "fix the bug that..."` - it's similar like snapshot. which is confirm, commit and upload into `.git` database to stores. **note:** you need describe more specific abt what you've done

if you delete a file, again, you need to write `git add file2.js`.<br>
then `git commit -m "removed unused code"`

### staging files

`touch file1.text` - to create new file

`echo hello > file1.txt` - to create new file similar with `touch` but it able adding note `"hello"`

`echo world >> file1.txt` - `>>` append

`git add file1.text`

`git add *.text`

`git add .`

**note:** be careful abt `.` to update large project, because it also give to store on git subdirectory 


### committing changes

`git commit -m "Initial commit."`

`git commit` - if you type this, it will automatically popup that you need to create description. 

### skipping the staging area

`git commit -am "fix the bug that prevent....` - `-am` add and message | into one statement | `git add .` + `git commit -m "fix the bug...."`


### removing files

`rm file2.txt`

`git status` - for checking

`git ls-files` - to check what current file with have

```
output:
file1.txt
file2.txt
```

`git add file2.txt` - to update that you've deleted file

`git ls-files` - to check again

```
output:
file1.txt

```

`git status`

`git commit -m "remove unused code"`


### renaming and removing files

`mv file1.txt main.js` - rename `file1.txt` into `main.js`

`git add file1.txt`

`git add main.js`

`git status` - `file1.txt -> main.js`

`git mv main.js file1.js` - `file1.txt -> file1.js`

----

`git status -s` - for quick summary for status

`git diff --staged` - to see what we have in the staging area that is going in the commit

```
output: 
diff --git a/file1.txt b/file1.txt
index 94954ab..badfb70 100644 {it's metadata. it's doesn't matter}
--- a/file1.txt
+++ b/file1.txt
@@ -1,2 +1,3 @@
 hello
 world
+test
```

<br>

`git diff`


## **diff tools**

step 1: `git config --global diff.tool vscode`

step 2: `git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"`

step 3: `git config --global -e` - to open vscode automatically

----

### viewing the History

`git log` - to see history

`git log --oneline` - to show history in a **short summary**

`git log --oneline --reverse` 

----

### viewing a commit

`git log --oneline`

`git show d601..` or `git show HEAD~1` - so that faster and no need to type unique number identifier 



----
skiped the video
time: 0:30:21 Skipping the Staging Area

