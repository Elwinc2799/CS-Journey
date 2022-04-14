# Useful Git commands

## Setup global configuration

Set global user
```
git config --global user.name "firstname lastname"
```

Set global email address
```
git config --global user.email "email_address@gmail.com"
```

Set global command line colouring for git command
```
git config --global colour.ui auto
```

## Initialize a project

Initialize current directory as git repository
```
git init
```

Clone a repository from github
```
git clone https://github.com/Elwinc2799/CS-Journey.git
```

## Stage files

Show all modified files
```
git status
```

Stage a file to the next commit
```
git add file.extension
```

Unstage a file from the next commit
```
git reset file.extension
```

Check which files is modified but not staged
```
git diff
```

Commit all staged files
```
git commit -m "commit message"
```

## Branch and merge

List all branches
```
git branch
```

Create a new branch
```
git branch new-branch-name
```

Checkout to the other branch
```
git checkout branch-name
```

Merge the specified branch to the current active branch
```
git merge branch-name
```

## Share and update

Push all local commits to the remote repository
```
git push
```

Update the local repository from the current remote branch
```
git pull
```

## Temporary commits

Save modified and staged changes
```
git stash
```

List all stacked-type stashed changes
```
git stash list
```

Pop out the top stashed changes
```
git stash pop
```

Discard the changes of the top stashed changes
```
git stash drop
```
