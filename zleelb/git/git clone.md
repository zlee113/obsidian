Date: 2024-07-14
Hub: [[Git]]
Tags: #book
URL/Title: Learning Git 

creates an exact copy of a remote repository as a local one, automatically selecting the shortname of the repository as origin, you can use the command git clone <URL> <directory_name> to clone a remote repo. If you do'nt include the directory name the repo will clone with the name of the remote repo. The step by step of the clone command is as follows:
1.  creates a project directory in the current folder
 2. initalizes the local repo
 3. downloads all the data from the remote repo
 4. adds a connection to the remote repo cloned from as origin as the shortname
 
when done cloning git needs to know which branch to be on, the origin/HEAD pointer determines which branch it is. This is the only local branch that will be on the cloned repo and only after the user switches onto a branch will it create a local version for the remote branches it has kept.