# Git

A minimal list of useful Git commands

## Global Config

```bash
git config --global user.email "e-mail"
git config --global user.name "first name last name"
```

## Branches
Create a new branch and switch to it.
```bash
git checkout -b my-feature
```

## Commit
Commit staged changes with a message.
```bash
git commit -m "my message"
```

## Sync with remote
Fetch all remote branches and remove deleted ones (prune = clean up).
```bash
git fetch --all --prune
```

Get the latest changes from the remote branch.
```bash
git pull
```

Send local commits to the remote branch.

```bash
git push
```