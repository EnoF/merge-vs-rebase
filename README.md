merge-vs-rebase
===============

A test project to display the advantages of rebasing over merging.

To display the advantages of rebasing over merging, I would need to add some more content to this `README.md`.

##The Jump
This paragraph will display that even when you have multiple commits, the you will not need to resolve the same conflict
more than once.

To test this run the following commands:

    git clone git@github.com:EnoF/merge-vs-rebase.git
    cd merge-vs-rebase
    git checkout -b rebase-test origin/jumping
    git rebase origin/master
    
The rebase will prompt you with a conflict. Resolve the conflict by adding the `introduction` first and the `jumping`
changes below. Then run:

    git rebase --continue

Notice that when you modify the line of the conflict once again, you will have to resolve the `original` conflict again.
