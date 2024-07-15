Date: 2024-07-14
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git 

Three-way merges occur when development history of the branches involved in the merge have diverged, so you can't get the target branch from the commit history. 

To resolve in practice you do two steps:
1. Fetch changes from the remote repo
2. Integrate changes locally in branch and repo
3. *Push local branch to sync remote branch*
When completing a three way merge you might notice a strategy of `ort` or `recursive`. This is basically saying that the merge was a three-way merge, if you also use the [[git cat-file]] with the p flag to see the parent of this commit it will show two parents for each commit used in the merge.

When this occurs but the users edit the same file we get a [[merge conflict]]. 