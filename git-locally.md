# Basic commands
- Git creates a .git directory and tracks the changes in the working directory (and subtree).
	- To create a .git/ folder:
		```
		$ git init
		```
	- Make a file in the working directory: 
		```
		$ cat > newFile
		```
		- Type some text, press return and Ctrl+D to exit (and save).
		- Alternative:
			```
			$ touch newFile
			```
	- Track the changes in the working directory:
		```
		$ git status
		```
		- This command shows the status of the files, untracked, staged.
			+ _untracked_ is the stage after the commit.
			+ _staged_ is the stage before you are ready to commit.

	- Add files to the staged step:
		```
		$ git add . # to add all the files
		$ git add newFile # to add only newFile
		```
		- Now the files are ready-to-commit.
			+ Retype: `$ git status # to see the difference`
	
	- Commit files:
		```
		$ git commit -m newFile # commits only <newFile>
		$ git commit -a -m . 	# 'commit all the files without the staging step (ie. git add)
		```
# Branching
- Making branches allows you to apply modification in a different branch, keeping intact the original code.
- Creating a new branch:
	```
	$ git branch NewBranch
	```
	- Switching to the new branch:
		```
		$ git checkout NewBranch
		```
		- Make a file in the new branch:
			```
			$ touch testFile # this file does not exists unless merge this branch to your master branch
					 # by default the master branch is named 'master' unless you renamed it
			```
		- Going back to your master branch:
			```
			$ git checkout master
			```
	- Merge NewBranch to master branch:
		```
		$ git merge NewBranch # at this point the 'testFile' is created
		```

