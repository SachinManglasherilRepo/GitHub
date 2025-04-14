Basic Setup Commands:
-------------------------
git config --global user.name "Your Name" ---->Set your Git Username
git config --global user.email "Your email" -->set your Git User email

git config --list  ---->List all git configurations


Initializing and cloning Commands:
-------------------------------------
git init --->initiates a new git repository in your project 

git clone <repo-url>  ----> clone an existing repository 


Working with Changes:
---------------------

git add <file>  --> stage a specific file for commit 

git add .   ---> stage all changes in current directory

git commit -m "commit changes"  ---->commit changes with a message 

git commit -am "message"   ----> add and commit tracked files in one step.

git commit --amend   ---->edit the last commit message or add changes to it.


Handling Merge Conflicts:
-----------------------
git diff   --->compare working directory changes.


git diff branch1 branch2 --->compare two branches.


Resolve conflicts: open the file,fix conflicts ,then add and commit 


Undoing Changes:
---------------
git reset file ----> unstage a file

git reset --soft HEAD-1  --> undo last commit but keep changes staged

git reset --mixed HEAD-1  -->undo last commit , keep changes in the working directory unstaged.

git reset --hard HEAD-1  --> completely remove the last commit 

git revert <commit-id> --> create a new commit that undoes the specified commit 


Stashing Changes:
-------------------

git stash ----> teporarily save changes.

git stash list -----> view stashed changes 

git stash pop ----> reapply stashed changes and remove them from the stash list 

git stash apply ----> Reapply stashed changes without removng them 

git stash clear ----> Remove all stashed entries.


Collabarating and pull request :
----------------------------------
git branch -a ---->list all branches including the remote .

git push origin <branch-name> ----> delete a remote branch 

#creating a PR : Go to your github repository ,select  your branch 
and click new PR.

Reviewing Changes:
-------------------
git show <file> ----> display changes made into a specific file.

git diff <commitid-1> <commitid-2> ----> compare changes between two commits.

Cleaning up :
--------------
git clean -f ---> remove untracked files.

git clean -fd --->remove untracked files and directories.

git gc --prune=now ---> clean up unnecessary files and optimize local repository.

Status and Logs:
----------------
git status ---> shows the current status of changes in the working directory.

git log ----> view commit history 

git log --oneline --->shows concise commit history 


Branching and Merging :
-----------------------
git branch <branch-name> -----> create a new branch 

git checkout branchname ------->switch to specific branch 

git checkout -b <branchname>  ---> create and switch to new branch 

git merge <branch-name>  ---->merge specified branch into current branch 

git rebase branchname -----> Reapply commits on top of another base 

git rebase -i HEAD-<n> --------> interactive rebase to edit commit history ,rearrange commits,modify commit messages
                                  or sqash the last n commits 

git branch -d branchname   ----> delete a local branch 


Remote Repositories 
--------------------
git remote add origin <url>----->link your local repository to a remote one 

git remote -v   ---> list the remote repository url 

git remote set-url origin <new-url> --->update the remote url for the repository 

git remote rename <old-name> <new-name> --->  Rename a remote 

git push -u origin <branchname> ----> push changes to remote repsoitory 


git pull origin <branchname> ----> pull changes from the remote branch 

git fetch -----> download updates from the url without merging 

git fetch <remote> ----> fetch updates from a specific remote 

Advanced Operations:
---------------------
git cherry-pick <commit-id> ----> Apply a specific commit from another branch 

git cherry-pick <start-commit-id><end-commit-id>  ----> cherry pick a range of commits

git tag <tag-name> ---->Add a tag to a commit 

git tag -d <tagname> ----> remove a local tag 

git reflog ----> view history of all changes ( even uncommited)

git reflog show <branch-name>  ----> show reflog for a specific branch 

git show <commit-id> ---> show detiled info for a specific commit 

git bisect start ---> start bisecting to locate a bug 












