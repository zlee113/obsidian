One way to integrate changes, a merge has two branches involved, the source branch containing the desired changes and the target branch that you're merging into

- two different kinds of merges, fast forward and [[three way merge]]
	- fast forward merge is taking the pointer of the target branch and moving forward to a new commit from the source branch, basically just doing some stuff on a new branch and merging it in no conflicts
	- [[three way merge]] is when we make a branch and develop on both the source and target branches making them both diverge from the parent commit of both of them causing merge conflicts. Either way git automatically makes a merge commit afterwards that needs to be pushed to complete the three way merge to sync the remote repo.