

extensions available for bringing additional git features for vs code
* gitLens -- Git supercharged


git GUI:
* GitKraken Git GUI (the most popular)
    * git cracking boards -- for issue tracking
    * git cracking timelines -- for project management
    * but need to pay in annually

* sourcetree (completely free)

---

but why command line instead of GUI?

* GUI tools have limitations
* GUI tools are not always available


---

posh-git - git GUI that you can see directory path in beautifully and colour

---
## **diff tools**
* KDiff3
* P4Merge
* WinMerge (Windows Only)
* VSCode

step 1: `git config --global diff.tool vscode`

step 2: `git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"`

step 3: `git config --global -e` - to open vscode automatically

---


