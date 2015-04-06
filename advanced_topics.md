#Advanced Topics

##Branching

* Each git branch represents a git object that points to the last branch's commit ([commit object](internals.md#object-files)). 
That is why it is very cheap operation in git to create a new branch.
* List of all branches (their heads) could be derived through `ls .git/refs/heads` command - it will display files where each stores reference on the corresponding branch's latest commit
