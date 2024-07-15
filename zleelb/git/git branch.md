Date: 2024-07-14
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git 

lists local branches, when used with a parameter after creates a new branch with that name off of the current commit for that branch. .git > refs > heads > name_of_branch should have the same commit hash and you can confirm by git log showing both branches for that specific commit you can use the:

```
git branch --all
```
Command to see all the local AND remote repos.

```
git branch -vv
```

See the list of local branches and their upstream branches.

you can also switch between branches using either [[git switch]] or [[git checkout]] and you can also use either to create a new branch

To define an [[upstream branch]] for a branch you can use:
`git branch -u shortname/branch_name`
to be able to use [[git push]] and [[git pull]] freely without having to define it and use -vv for verbosity if you want to know if its been defined already.