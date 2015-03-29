# REMOTES
- Remotes gives you the possibility to clone a repository which lives online.
- You can also push your changes online.
- Or propose changes with pull (fetch is unclear yet).
- Check your remote:
	
	`$ git remote 	# this should return 'origin'
			# in order to access a remote you have first to git clone <URL>
			# To initialize a remote in your github account do it using a web browser (I am not sure how to do this in command line).`
- Show remote's URL:
	`$ git remote -v`

- Fetching/Pulling (?):
	`$ git fetch origin 	# shows changes since last fetching the server`
	`$ git pull 	  	# updates your local repository(?) - I use this in orgmode (also propose changes..)`

- Push online:
	`$ git push origin master # uploads your master branch to the origin`
