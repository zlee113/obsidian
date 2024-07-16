Date: 2024-07-14
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git 

Use to fetch data (same as [[git fetch]]) from a remote repo and integrate it into a branch in a local repo in a single go. 
```
git pull <shortname> <branch_name>
```
If an [[upstream branch]] is not set you need to use the full command, and if not you can simply use 
```
git pull
```
and it will automatically use whatever is defined.

Assuming the histories of the remote branch and the local branch have not diverged the pull will simply perform a [[fast forward merge]]. Otherwise you have to tell the command whether you want to use [[git merge]] or [[git rebase]]. 

Similar to [[git fetch]] git pull also has a prune option with the p flag:
```
git pull -p
```