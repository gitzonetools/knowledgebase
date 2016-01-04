## Git
### How to generate SSH Key for Github/Bitbucket

type in a terminal:

```sh
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
# Creates a new ssh key, using the provided email as a label
# Generating public/private rsa key pair.
```

> TIP: store the result with a unique filename in your accounts ~/.ssh directory

then copy the key to the public desired machine

```sh
ssh-copy-id -i [yourcustomname].pub [username]@[serverhost]
```

### Make current commit the intial commit:

```sh
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