Date: 2024-07-15
Hub: [[Git]]
Tags: #book #web 
URL/Title: Learning Git,  https://blog.git-init.com/how-to-undo-changes-in-git-using-reset-revert-and-restore/

Restores a file to another version, specifically for restoring a file added to the [[staging area]] that you want removed you can do the following:
```
git restore --staged <filename>
```

Using the command by itself will simply restore the current version of a file to what it was at the last commit, perfect for undoing any changes since, but does delete so careful when using.
```
git restore <filename>
```