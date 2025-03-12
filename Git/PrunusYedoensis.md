# PrunusYedoensis x Git

Dedicated to Git.

## VS Code

Change the ` username ` and ` email ` under the ` user ` section.  
To change the credentials to use for Git commits, go to the following path...

### macOS

` /Users/{name}/.gitconfig `

### Windows

` ? `

## Error on commit

`git reset --soft HEAD~1` :

- Cancel the previous Commiti
- Leave the changes of the files prepared for the Commit (Staged)
- The files remain modified and ready to be cloudy again

`git reset --mixed`/`git reset` :

- Cancel the previous Commit
- Leave the file changes in the Working Directory (Non Staged)
- The files remain modified, but are no longer prepared for the Commit
