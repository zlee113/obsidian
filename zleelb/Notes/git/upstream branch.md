Date: 2024-07-14
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git 

the upstream branch is the remote branch the local one is tracking that you can set explicitly

a remote branch that a particular local branch tracks. Cloned repos automatically set up upstream branches. Two main benefits for defining upstream branches
1. if you fetch the remote repo commits you can check if the repo is ahead or behind the remote repo with git branch -vv or git status
2. simplifies commands as you don't need to specify the upstream branch

To define an upstream branch for a repo you can use [[git branch]] with the -u flag which is short for --set-upstream-to and then the remote repo [[shortname]]
