# Git-Guide
Basic commands guide for git and git flow.

## Git Commands

### Start project

```
git init
```

```
git clone
```

### Connection to repository

```
git remote -v
```

```
git remote add <name> <url>
```

```
git remote rename <oldname> <newname>
```

```
git remote remove <name>
```

### Branches

```
git branch
```

```
git branch <branchname>
```

```
git branch -m <oldbranch> <newbranch>
```

```
git branch -d <branchname>
```

### Checkout

```
git checkout <branchname>
```

```
git checkout -b <newbranch>
```

### Status & Log

```
git status
```

```
git log
```

```
git log --oneline
```

### Add & Commit

```
git add <file>
```

```
git add .
```

```
git commit -m "<msg>"
```

### Tag

```
git tag <tagname>
```

### Push & Pull

```
git push <remotename> <branchname>
```

```
git pull <remotename> <branchname>
```

## Git Flow Commands

### Config

```
git flow init
```

### Feature

```
git flow feature start <newbranch>
```

```
git flow feature publish <branchname>
```

```
git flow feature finish <branchname>
```

### Release

```
git flow release start <newbranch>
```

```
git flow release publish <branchname>
```

```
git flow release finish <branchname>
```

### Hotfix

```
git flow hotfix start <newbranch>
```

```
git flow hotfix publish <branchname>
```

```
git flow hotfix finish <branchname>
```
