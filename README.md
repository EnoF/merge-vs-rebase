merge-vs-rebase
===============

A test project to display the advantages of rebasing over merging.

To display the advantages of rebasing over merging, I would need to add some more content to this `README.md`.

##Introduction
This introduction paragraph will be modified by the branch `intromod` and `introcon`. The branch `jumping` will be 
having a conflict with this introduction paragraph for the first commit. The rest of the commits should not contain any 
further conflicts.

##Finalize
Lets wrap everything up and get all branches together in `merge` style and `rebase` style.

###Merge

    git checkout -b merge-final origin/master
    git merge intromod
    git merge introcon
    git merge jumping
