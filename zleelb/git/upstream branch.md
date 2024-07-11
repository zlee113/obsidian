the upstream branch is the remote branch the local one is tracking that you can set explicitly

a remote branch that a particular local branch tracks. Cloned repos automatically set up upstream branches. Two main benefits for defining upstream branches
1. if you fetch the remote reop commits you can check if the repo is ahead or behind the remote repo with git branch -vv or git status
2. simplifies commands as you don't need to specify the upstream branch