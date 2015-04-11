# Inspecting a Repository

## git show

Show various types of objects.

* **git show `commit`** - shows information about `commit` including all the changes that were introduced by it. Very usefull command if you would like to view a `diff` between particular commit and its parent

## git log

Displays commited snapshots. This command operates only on commited history (in contrast with `git status` command which operates on staged files).
By default displays an entire commit history with default formatting.

* **git log -n `limit`** - limits the number of commits by `limit`
* **git log --oneline** - condences each commit description to a single line
* **git log --decorate** - will add branchs' and tags' names to the output
* **git log --stat** - includes the info regarding which files were altered and relative number of lines that were added/deleted
* **git log -p** - displays a "patch" for each commit - diff for each commit. This option leads to the most verbose output

* **git log --author=`pattern`** - search for commits of the particular author

* **git log `since`..`until`** - lists commits from which `since` commit (branch, tag, HEAD ref) could be reached but the `until` could not
* **git log --since=`2.weeks`** - displays commits of the specific period. Period parameter could have vareity of formats - you can specify date like `2008-01-15` or a relative date such as `2 years 1 day 3 minutes ago`

* **git log --grep=`pattern`** - search for commits with a `pattern` in a commit message.
* **git log -S`function-name-or-any-pattern`** - displays commits that contain specified pattern. Very useful option for searching changes of specific function.

* **git log `file`** - only lists commits of the particular file. Usefull for viewing history of a particular file. Should be placed after the double dash `--` separator in case if combined with another options

### Popular usage examples

* **git log --graph --decorate --oneline** - graph representation of project history with all necessary tags being added

### Notes

* Tilda `~` character is aimed to simplify the process of referencing commits that are relative to the other. For example, in order to view the differences between commit `2e4a..` and its parent, the following command could be used: `git log 2e4a~1..2e4a`
* The `git log` command is typically a starting point for finding a commit that you would like to operate on



