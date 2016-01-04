## Git
### How to generate SSH Key for Github/Bitbucket

type in a terminal:

    $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    # Creates a new ssh key, using the provided email as a label
    # Generating public/private rsa key pair.

store the result with a unique filename in the accounts .ssh directory

then use

    ssh-copy-id -i [yourcustomname].pub [username]@[serverhost]
    
You'll be guided by a wizard through the creation of a SSH key.

### Make current commit the intial commit:
```
git checkout --orphan newBranch
git add -A  # Add all files and commit them
git commit
git branch -D master  # Deletes the master branch
git branch -m master  # Rename the current branch to master
```

### Go one commit back and ommit the latest commit

```
git reset --hard HEAD~1
git push origin <branchname>
```

### Show the branch you are in in the CLI
Have a look here:
[https://github.com/jimeh/git-aware-prompt](https://github.com/jimeh/git-aware-prompt)