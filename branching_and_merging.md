#Branching and Merging

A branch represents an independent line of development. Each branch results in a forking of the history of the project.

##git branch

Lets create, list, rename and delete branches. It does not let you switch between branches - that's why it is tightly integrated with the `git checkout` and `git merge` commands

* **git branch** - list all branches in the repository
* **git branch `branch_name`** - create a new branch
* **git branch -d `branch_name`** - deletes branch only if it has been merged to the current branch
* **git branch -D `branch_name`** - forced branch deletion
* **git branch -m `new_branch_name`** - renames current branch to `new_branch_name`

### Notes 
* It is a quite good practice to consider new branch creation whenever you've decided to implement new feature or fix the bug - and there is no matter how large or small this fix is.
* Branch helps encapsulate changes in order to clean commits history afterwards before merging. Thus, branches help keep main (master) branch free from questionable code.
* It is important to understand that branches are just [pointers to commit object](advanced_topics.md#branching) - they are very lightweight.
* In order to switch between branches `git checkout branch_name` command should be considered.

### Deleting branches
* If you will try to use `git -d branch_name` without preliminary merging you will obtain a warning message and abort of the deletion operation. This behavior is intentional and aims to protect you from the possibility of loosing the entire line of the development due to the fact that after deletion of branch's head its commits would become unreachable without merging.
* If you really want to delete the branch, use `git -D branch_name` instead

## git checkout 

Provides a way of switching between existing branches. Think of it as a way of switching between development lines.

* **git checkout `existing-branch`** - switch to (checkout) the specified branch. Git will try to preserve all changes that were made between switching - in case when switching procedure will introduce conflicts Git will reject it
* **git checkout -b `new-branch`** - a shorthand command for creating a branch and switching to it afterwards. An equivalent for `git branch new-branch`, `git checkout new-branch`

### Notes

`git checkout` works hand-in-hand with `git branch`. If you'd like to commense a work on a new feature, a new branch should be created with the `git branch` and HEAD pointer should be switched to it with `git checkout` afterwards. For each particular feature should be introduced its corresponding branch - it makes it very easy to try any experiments while working on different features at the same time.

### Detached HEAD

Remember that HEAD always pointing to the current latest commit. In ***Detached HEAD*** state it points not on the latest commit of any of the branches - it warns that any changes to that particular state will be lost due to the fact that those will be introduced as an appendix of the branch's development line - there will be no any branch that will point to this new commit afterwards. In order to save your experiments in ***Detached HEAD*** state you should introduce an additional branch and save new commits to it.




