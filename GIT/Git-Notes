==========
Phase-1
==========
# What is VCS. Why we need VCS.
	VCS features.

#
GIT Installation (Ubuntu):
$ sudo apt-get update
$ sudo apt-get install git

Verify Installation:   
	which git
	git --version

GIT Uninstallation:
$ sudo apt-get remove git

#
Setting up mandatory configurations:
=============================================
$ git config --global user.name "swapnil"
$ git config --global user.email "abc@gmail.com"

Check the configurations using below command
$ git config --list

Git stores all configurations in below file
"cd /home/swapnil/.gitconfig"

=========
Phase-2
=========
Creating remote repository in github
===============
1. create an account in github.com
	URL: https://github.com

2. login github.com with your credentials. 	
     	click on "new repository" --> "create reopository" 

3. copy the repo URL from Github:
	https://github.com/<github-username>/REPO-NAME.git

4. Clone the source code from remote repository using 'git clone' command
	$ git clone https://github.com/<github-username>/REPO-NAME.git

5. 	$ cd REPONAME

6. Create some sample code and submit the code to remote repo.
 
	    $ vim Login.java  

	    $ git status

	    $ git add Login.java or git add .

	    $ git commit Login.java -m "login module code"
		
	    $ git push
	     UN and pwd(token)

#
Git Architecture Diagram

	------------------------------------------------------	
	. (Souce area) | ..(Stage) | .git (Local Repository) |
		       |           |			     |
	------------------------------------------------------

========
Phase-3
========
# History - Deep Dive
	$ git log <filename>
	$ git log

	Options:
		- git log -n2
		- git log --author="swapnil"
		- git log --grep="commit msg"		
		- git log --oneline (if we want to see logs on high level that time we can use this command ie. only commit ids and msg)
		
=========
Phase-4
=========
 
#If you want downlod remote repository then apply this commnad (It is first time activity).
	$ git clone <repo-url>

#If you want to download modified content from remote repo then apply this command, after git pull your modified changes comes in working area.
	$ git pull

#If you want to download modified content from remote repo then apply this command, But you dont want to merge modified content in your working area then apply this command
	$ git fetch
	$ git merge

# Skip staging
	git commit -am "submit all pending changes"

# 
Creating up Local repository
1. create/initialize a local repository with 'git init' command
	$ mkdir <create-folder>
	$ cd <folder-name>
	$ git init
	$ vim filename
	$ git add . or filename
	$ git commit -m "commit msg"
(Note - Create same folder name repositry in the github server)
	$ git remote add <repo-name> <repo-url>
	$ git push <repo-name> 
  	$ git push --set-upstream <repo-name> master (optional)

2. Observe the local repository
	$ ls -a 

3.create some source code.. ex: vim Login.java

4.Adding the file to STAGE.
	$ git add <filename>

5.Commiting the file to local repository
	$ git commit <filename> -m "lgoin module code"

6.Check the log of Login.java using log command.
	$ git log <filename>


=======
Phase-5
=======
# GIT Commands

1.
	$ git status 

	$ git diff <filename>

	$ git diff --staged <filename> 

2. Deleting a file

	A.) $ git rm <filename>
	    $ git commit <filename> -m "comment"
	    $ git push
       
4. Renaming a file/folder
	A.) $ git mv Login.java <new-name>
	    $ git commit -m "rename Login"
	    $ git push


=======
Phase-6
=======

# Undoing the changes:

# undo/revert local changes from source area in exits files. ie. present in remote repo.
	$ git checkout <filename>

# Unstage the changes from STAGE area
	$ git reset HEAD <filename>

# Move changes from .git to source area 
	$ git reset --mixed HEAD~1

# Move changes from .git to stage area
	$ git reset --soft HEAD~1

# Remove changes from everywhere
	$ git reset --hard HEAD~1

=======
Phase-7
=======

# BRANCHING
	A. What is a branch?
	B. Why and When we create a branch?
	C. Branching Stratogy overview


# List all the branches
	$ git branch
	
# Creating a new branch
	$ git branch new_branch_name

# List all remote branches
	$ git branch -r

# Switching to a newly created branch
	$ git checkout new_branch_name

# Creating and switching to a newly created branch
	$ git checkout -b new_branch_name

# First push newly created branch into remote repo
	$ git remote add <repo-name> <repo-url>
	$ git push --set-upstream <repository-name> <branch-name>
		or
	$ git push --all
		or
	$ git push -u origin --all

# List all remote branches
	$ git branch -r

# Merge files from source branch to target branch
	$ git merge <source-branch-name>

# HEAD
HEAD is a pointer in git which
	- Always points to the latest commit in the repository
	- Always points to tip of the current reposiotory
	- Always points to parent of the next commit

Day-8
======
Merging:
======
# FAST-FORWARD MERGE

Excercise:
===========
# List all the branches
	$ git branch

# Create a new branch
	$ git branch dev_1.2.3

# Add some changes to newely created branch i.e dev_1.2.3
	$ Modify/Add some files	
	$ git add	
	$ git commit 

# Now merge the code from dev_1.2.3 to master branch
  Before merge, make sure that you are on target branch i.e master (source branch: dev_1.2.3)
	$ git checkout master

# You have master code in source since currently checkout branch is master. Now bring/merge the changes from dev_1.2.3 to master by running below command. 
Git merge command merges the changes from dev_1.2.3 to master.

	$ git merge dev_1.2.3

# observe the changes from dev_1.2.3 into master branch.

# git push --all

============
# Real Merge
============

MERGING With CONFLICT:
============

# List all the branches
	$ git branch

# Create a new branch
	$ git branch release1.0


# Take a file which is common in master and release1.0 branch.
  ex: Login.java

# Make sure Login.java has below content in master and release1.0 branch
	Login.java
		line#5 --> int a = 10;
	
# To create a conflict situation, we need to modify same line in two branches with different content.

	ex: Login.java (master)
			line#5 --> int a =100;
		
		Login.java (release1.0)
			line#5 --> int a = 200;


# Now merge the code from release1.0 to master branch
  Before merge, make sure that you are on target branch i.e master (source branch: release1.0)
	$ git checkout master

# You have master code now, since currently checkout branch is master. Now bring/merge the changes from release1.0 to master by running below command. 
Git merge command merges the changes from release1.0 to master.

	$ git merge release1.0

# Run git status command to list conflict file

#Resolve the conflict and commit the merge

# Run git push command to move the merge to Remote.


# What is Conflict:
If two users modify the same file in source and target branches and if the same line has different content, git can't decide which user's code it has to take. we call this situation as conflict.

# How do you resolve the conflict: 
- Open the conflict file--> remove conflict markers-->select the right content.
- git add
- git commit
- git push --all

# How to delete branch from local
git branch -d/-D <branchName> (the -D option is for force deletion)

How to delete remote branch from local
git push origin -d <branchName> or git push origin :<branchName>

git cherry-pick <sha-value>

git stash

git stash pop
