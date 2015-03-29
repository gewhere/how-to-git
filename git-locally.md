# Basic commands
- Git creates a .git directory and tracks the changes in the working directory (and subtree).
	- To create a .git/ folder:
		```bash
		$ git init
		```
	- Make a file in the working directory: 
		```bash
		$ cat > newFile
		```
		- Type some text, press return and Ctrl+D to exit (and save).
		- Alternative:
			```bash
			$ touch newFile
			```
	- Track the changes in the working directory:
		```bash
		$ git status
		```
		- This command shows the status of the files, untracked, staged.
			+ _untracked_ is the stage after the commit.
			+ _staged_ is the stage before you are ready to commit.

	- Add files to the staged step:
		```bash
		$ git add . # to add all the files
		$ git add newFile # to add only newFile
		```
		- Now the files are ready-to-commit.
			+ Retype: `$ git status # to see the difference`
	
	- Commit files:
		```bash
		$ git commit -m newFile # commits only <newFile>
		$ git commit -a -m . 	# 'commit all the files without the staging step (ie. git add)
		```
# Branching
- Making branches allows you to apply modification in a different branch, keeping intact the original code.
- Creating a new branch:
	$ git branch NewBranch
	
	- Switching to the new branch:
		$ git checkout NewBranch

		- Make a file in the new branch: 
			$ touch testFile # this file does not exists unless merge this branch to your master branch
					 # by default the master branch is named 'master' unless you renamed it

		- Going back to your master branch:
			$ git checkout master
		
	- Merge NewBranch to master branch:
		$ git merge NewBranch # at this point the 'testFile' is created

# REMOTES
- Remotes gives you the possibility to clone a repository which lives online.
- You can also push your changes online.
- Or propose changes with pull (fetch is unclear yet).
- Check your remote:
	$ git remote 	# this should return 'origin'
			# in order to access a remote you have first to git clone <URL>
			# To initialize a remote in your github account do it using a web browser (I am not sure how to do this in command line).

- Show remote's URL:
	$ git remote -v

- Fetching/Pulling (?):
	$ git fetch origin 	# shows changes since last fetching the server
	$ git pull 	  	# updates your local repository(?) - I use this in orgmode (also propose changes..)

- Push online:
	$ git push origin master # uploads your master branch to the origin
