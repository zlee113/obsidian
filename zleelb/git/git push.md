Used to push local changes to the [[upstream branch]]. If the upstream branch is set you can push with no arguments and it will push automatically to it. You can also state the [[shortname]] and branch name as in: 
`git push <shortname> <branch_name>` 
which will upload from the branch of the local repo to the [[shortname]] remote repo as an individual branch.

deleting a branch is used to declutter and remain organized. it is important to make sure all commits on the branch are merged onto another branch first, even though the commit won't be lost it will be annoying to attempt to access with no branch. you can delete a local branch using the [[git branch]]  command with the -d option and a local branch on a remote repo with the push command with the -d option as:
`git push <shortname> -d <branch_name>`

ERRORS:
Git will only let you push if you integrate remote changes first before integrating new ones. So if the remote branch is updated before you push you must integrate those changes before you can push.
