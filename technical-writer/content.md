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

When this happens, your local branch needs to be synchronized with the remote branch with git pull or git fetch and git merge.`git fetch` again takes our current branch, and checks to see if there is a tracking branch. If so, it looks for changes in the remote branch, and pulls them into the tracking branch. It does not change your local branch. To do that, you'll need to do `git merge origin/master` (for the "master" branch) to merge those changes into your branch - probably also called "master".`git pull` simply does a `git fetch` followed immediately by `git merge`. This is often what we desire to do, but some people prefer to use git fetch followed by git merge to make sure they understand the changes they are merging into their branch before the merge happens.
