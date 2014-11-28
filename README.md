merge-vs-rebase
===============

A test project to display the advantages of rebasing over merging.

To display the advantages of rebasing over merging, I would need to add some more content to this `README.md`.

##Introduction
This introduction paragraph will be modified by the branch `intromod` and `introcon`. To display the effect an merge 
commit, we will create some commits in between. The merge commit will have several effects on your git history:
 * Your history will display multiple history lines
 * Your history will not be able to rebase before the merge commit without a force push


To test this we will do it for both `merge` and `rebase`. Lets first start with a `merge`.

    git checkout -b merge-intro origin/master
    git merge origin/intromod
    git merge origin/introcon

Now lets test a `rebase`:

    git checkout -b rebase-intro origin/intromod
    git rebase origin/introcon

The branch `jumping` will be 
having a conflict with this introduction paragraph for the first commit. The rest of the commits should not contain any 
further conflicts.##Finalize
Lets wrap everything up and get all branches together in `merge` style and `rebase` style.

###Merge

    git checkout -b merge-final origin/master
    git merge origin/intromod
    git merge origin/introcon
    git merge origin/jumping

###Rebase

    git checkout -b rebase-final origin/jumping
    git rebase origin/introcon
    git rebase origin/jumping
    git rebase origin/master
