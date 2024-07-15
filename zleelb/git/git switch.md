Date: 2024-07-14
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git 

Used specifically to only switch branches, encapsulated by the git checkout command but more limited in scope and less popular

```
git switch <branch_name>
```

Switch command does three things when using
1. Changes HEAD pointer to branch being switched to
2. populates staging area with snap of commit
3. copies contents of staging area into working directory

```
git switch -c branch_name
```

Use to create a new branch, [[git checkout]] has similar functionality but also switches to that branch in the same line