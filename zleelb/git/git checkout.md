Date: 2024-07-14
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git 
##### Notes: 
Used to switch branches but can also be used to switch to specific commits, doing this causes the detached head state so the [[HEAD]] isn't necessarily longer pointing to the most recent commit for a branch but any specific commit

```
git checkout -b branch_name
```

Creates a new branch similar to [[git switch]] but also switches to that branch automatically