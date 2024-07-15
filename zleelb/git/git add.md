Date: 2024-07-14
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git

Puts an untracked file that's in the [[working directory]] and adds it to the staging area. Once added it becomes tracked and git will now version control it. 

```
git add <file>
```
Adds one file
```
git add <file> <file> <file>...
```
Adds several files at once
```
git add -A OR git add .
```
Adds all new or modified files at once

NOTE: If you add a file and DO NOT commit and then make more edits only the version of the file when you used git add is in the [[staging area]] and will be committed you must use git add again with the file for it to be added.