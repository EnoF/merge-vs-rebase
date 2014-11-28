merge-vs-rebase
===============

A test project to display the advantages of rebasing over merging.

To display the advantages of rebasing over merging, I would need to add some more content to this `README.md`.

##Introduction
This introduction paragraph will be modified by the branch `intromod` and `introcon`. 

To test this we will do it for both `merge` and `rebase`. Lets first start with a merge.

    git checkout -b merge-intro origin/master
    git merge origin/intromod
    git merge origin/introcon

The branch `jumping` will be 
having a conflict with this introduction paragraph for the first commit. The rest of the commits should not contain any 
further conflicts.