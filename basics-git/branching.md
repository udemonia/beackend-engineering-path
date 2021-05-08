# Branching

## Master

> Should be the stable version of your code

## staging and commits

git add .

git commit -m "a note about the commit"

## branching

If you're on the master branch, you might want to make changes to a clone, preserving the master branch and its inherent stability

git branch {{ name }} _create a branch_

git branch -a _see all open branches the * means you're on the branch_

git checkout {{ branch name }} _switch to a branch_

git branch -d {{ branch name }} _remove a MERGED branch_

git branch -D {{ branch name }} _remove a un-merged branch_