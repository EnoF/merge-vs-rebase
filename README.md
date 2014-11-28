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
further conflicts.

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

To avoid such redundant commits, you can kill the unnecessary commit. In this example, the commit should be squashed
with the initial commit changing the header to fit the actual need. You will benefit of a cleaner history and the merge 
conflicts will be easily resolvable due to the small change sets per commits.
    
##Finalize
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
