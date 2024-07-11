In git, fetch represents retrieving information from a remote repo into a local one or just downloading data.

`git fetch <shortname>`
Downloads all data form remote repo with [[shortname]]

`git fetch`
Downloads all data from remote repo origin

Note: Does not integrate anything into the local repo only downloads it, points shortname/branch for whatever was downloaded from the remote repo to the commits downloaded but leaves all local ones alone

git fetch will also not automatically delete branches that no longer exist for the remote repo so utilizing the fetch command with pruning enabled will remove REMOTE tracking of those branches
`git fetch -p`
