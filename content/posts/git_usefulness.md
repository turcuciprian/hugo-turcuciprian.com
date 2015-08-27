+++
date = "2015-08-27T23:32:45+03:00"
description = "Useful basic git commands"
title = "Useful Git commands"
+++

### Initialize git in a working directory

So you have a directory where you want to set up git in. You cd into that directory and you do
```
git init
```
That's all it takes to have git initialized in that directory. 

### Connect to a remote repository 

Now what you want is to connect that git instance to a remote branch. To do this run:
```
git remote add origin <URL>
```
Now you're connected to a remote repo.Next you need to pull down the content from the repository.
To do this run:
```
git pull origin master
```
Basically git pull is a git fetch and a git merge. More information here: http://git-scm.com/docs/git-pull
### Add, Commit, Push

Once you modified a file, created one or deleted one, you need to let your remote branch know of the chage and push that change. To do so First you need to add your change. Run:
```
git add .
```
Where . just adds everything in that tree.
For a complete list of commands see: http://git-scm.com/docs/git-add

Then you can check your soon to be commit with:
```
git status
```
This one has options too. Available here: http://git-scm.com/docs/git-status

Then you do a commit:
```
git commit -a -m "Your message goes here"
```
-a commits all the files that have been told to git about in the previous add . command
-m is for the commit message
More commands here: http://git-scm.com/docs/git-commit

And then you push:
```
git push origin master
```
Where you are pushing to the master remote branch the local origin branch.

### Git branching

To create a branch do
```
git branch branchname
```
You have to be in the branch you want to duplicate. So if you're in master you do the above command to branch master.

Then you need to switch to that branch

```
branch checkout branchname
```
At this point you switched from what ever branch you where in, to this one. Now the changes in the previous branch are gone, you only have the changes in the branch. checkout is like the cd of git. More commands here: http://git-scm.com/docs/git-checkout

You can checkout brances or even commits.

### Reseting

```
git reset --hard
```
--hard
Resets the index and working tree. Any changes to tracked files in the working tree since <commit> are discarded.

--merge
Resets the index and updates the files in the working tree that are different between <commit> and HEAD, but keeps those which are 
different between the index and working tree (i.e. which have changes which have not been added). If a file that is different between <commit> and the index has unstaged changes, reset is aborted.
More information here: http://git-scm.com/docs/git-reset

### Revert

If you want to revert to a specific commit all you have to do is:
```
git revert <commit-code>
```
More information here: http://git-scm.com/docs/git-revert
