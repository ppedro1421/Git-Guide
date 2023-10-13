# Git-Guide

Basic commands guide for git and git flow.

<div style="width: 100%; background-color: white;">
    <img src="./assets/gitflow-1.png" alt="gitworkflow"/>
</div>

## Git Commands

### Start project

Create an empty Git repository.
```
git init
```

Clone a repository ``<url>`` into a new directory.
```
git clone <url>
```

### Connection to repository

Show remotes url after name.
```
git remote -v
```

Add a remote named ``<name>``  for the repository at ``<url>``.
```
git remote add <name> <url>
```

Rename the remote named ``<oldname>`` to ``<newname>``.
```
git remote rename <oldname> <newname>
```

Remove the remote named ``<name>``. 
```
git remote remove <name>
```

### Branches

List existing branches.
```
git branch
```

Create the new branch named ``<branchname>``, but it will not switch the working tree to it.
```
git branch <branchname>
```

Rename the branch named ``<oldbranch>`` to ``<newbranch>``.
```
git branch -m <oldbranch> <newbranch>
```

Delete branch named ``<branchname>``.
```
git branch -d <branchname>
```

### Checkout

Switch to branch named ``<branchname>``.
```
git checkout <branchname>
```

Create the new branch named ``<branchname>`` and switch to it.
```
git checkout -b <newbranch>
```

### Status & Log

Show the working tree status.
```
git status
```

Show commit logs.
```
git log
```

Show commit logs formated on oneline.
```
git log --oneline
```

### Add & Commit

Add file named ``<file>`` to br commited.
```
git add <file>
```

Add everything to be commited.
```
git add .
```

Record changes to the repository with message ``<msg>``.
```
git commit -m "<msg>"
```

### Tag

Create tag for current commit named ``<tagname>``.
```
git tag <tagname>
```

### Push & Pull

Send or update branch ``<branchname>`` to remote ref ``<remotename>`` .
```
git push <remotename> <branchname>
```

Fetch branch ``<branchname>`` from remote ref ``<remotename>`` and integrate with another repository or a local branch.
```
git pull <remotename> <branchname>
```

## Git Flow Commands

### Config

Configures git flow, creates branch develop if dont exist and let you name your supporting branch prefixes.
```
git flow init
```

### Feature

Create new feature branch named ``<newbranch>``.
```
git flow feature start <newbranch>
```

Push feature branch named ``<branchname>`` into remote.
```
git flow feature publish <branchname>
```

Merge feature branch named ``<branchname>`` to develop branch and remote then delete feature branch.
```
git flow feature finish <branchname>
```

### Release

Create new release branch named ``<newbranch>``.
```
git flow release start <newbranch>
```

Push release branch named ``<branchname>`` into remote.
```
git flow release publish <branchname>
```

Merge release branch named ``<branchname>`` to main branch, creates a tag then merge to develop branch.
```
git flow release finish <branchname>
```

### Hotfix

Create new hotfix branch named ``<newbranch>``.
```
git flow hotfix start <newbranch>
```

Push hotfix branch named ``<branchname>`` into remote.
```
git flow hotfix publish <branchname>
```

Merge hotfix branch named ``<branchname>`` to main branch, creates a tag then merge to develop branch.
```
git flow hotfix finish <branchname>
```
