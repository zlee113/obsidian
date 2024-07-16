Date: 2024-07-15
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git 

On the branch you want to rebase use the rebase command as so:
```
git rebase <branch_name>
```
This will reapply the commits on top of a branch as NEW commits with different hashes as the other commit(s). 

Now whats happening under the hood with the 5 steps of rebasing:
1. Find the common ancestor
2. Store info about the branches involved
3. Resets the HEAD to point to the same commit as the one being rebased to
4. It will then apply and commit the changes added onto it
5. Switches onto the rebased branch
This will all occur automatically assuming there isn't any conflicts with any of the commits.

If a [[merge conflict]] occurs the rebase will pause and you will need to go in and fix the conflicts. At that point you can either decide to continue with the next commit or abort with either flag:
```
git rebase --continue
```
```
git rebase --abort
```
