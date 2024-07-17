Date: 2024-07-14
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git 

When two branches are merged that have edits to the same part of a file or a file was deleted in one and not the other. This can occur from merging or rebasing with [[git merge]] or [[git rebase]]. 

These conflicts will be represented in the file with both sets of changes and will need to decide what to keep and then add to the [[staging area]] and commit. 
![[Pasted image 20240714143534.png]]
It will resemble this in the actual file, we see the same thing is vscode but vscode will show us a button saying which one to keep so we don't have to manually remove a lot of it.

#### Resolution Steps:
1. After using [[git merge]] when a conflict arises git will mark all the lines using the formatting above. Edit the file according to the changes you wish to see reflected and save the file/s. 