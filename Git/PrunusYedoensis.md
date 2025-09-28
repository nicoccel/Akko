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

## Command

- Commit

    ```git
    git add -A
    git commit -m "Text..."
    git push -u origin master
    ```

- Squash

    ```git
    git reset --soft HEAD~N
    git commit -m "Text..."
    git push --force-with-lease origin main
    ```

- Cancel last commit [NOTE](https://stackoverflow.com/a/927386/21670678)
- Stash all file [NOTE](https://stackoverflow.com/a/835561/21670678)
- Restore file stashed [NOTE](https://stackoverflow.com/a/19003191/21670678)
- View file on stash [NOTE](https://stackoverflow.com/a/10726185/21670678)
- Delete all file on stash [NOTE](https://stackoverflow.com/a/11369406/21670678)
- Abort merge [NOTE](https://stackoverflow.com/a/102309/21670678)
- Fetch `git fetch origin`
- Pull `git pull origin`
- Status `git status`
