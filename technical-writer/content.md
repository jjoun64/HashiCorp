# What is the Difference Between the Push, Pull, and Fetch Git Commands?

The following commands enable you to send, get, and merge changes between Git branches and repositories (also known as repos). This document will explain the diffferences between the commands.

- `git push` - Sends changes from a local branch to a remote repo
- `git fetch` - Gets changes from a remote repo into a local branch
- `git pull` - Gets and merges changes from a remote repo into a local branch

## Pushing changes

 The `git push` command enables users to share code with a remote repository. After you push changes from your local branch to a remote tracking branch, the tracking branch resembles the local branch.

This command checks if there is a tracking branch for your local branch located in a remote repository connected to your local repository. If so, Git pushes the committed changes from your working branch to the tracking branch. 
 
This operation will fail if the tracking branch has diverged from your local branch&mdash;the tracking branch contains committed changes that are not in your local branch. 

## Fetching and pulling changes

When the `git-push` command fails, synchronize your local branch with the tracking branch, using the `git fetch` and `git merge` commands or the `git pull` command. 

The `git fetch` command checks if there is a remote tracking branch for your local branch. If so, it pulls changes from the tracking branch into your local branch but does not change it. To incorporate the changes into the local branch, use the `git merge` command. 

The `git pull` command automatically runs the `git fetch` and `git merge` commands.

To understand the changes that you are pulling into your branch before merging them, use the `git fetch` command. If the changes are acceptable, follow up with the `git merge` command. 

Otherwise, use the `git pull` command.
