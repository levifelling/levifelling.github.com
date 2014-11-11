---
layout: post
title: Reference - GIT
---


## Create branch with detached head
```bash
# create detached branch
cd <existing repo>
git symbolic-ref HEAD refs/heads/<branchname>
rm .git/index
git clean -fdx

#add all your files
git add .
git commit -a -m 'initial commit'
git push origin <branchname>
```

## remove SVN remnants
```find . -name ".svn" -exec rm -rf {} \;```

## checkout a single branch of a git repo
```bash
mkdir <branchname>
cd <branchname>
git init
git remote add -t <branchname>-f origin <REMOTE_REPO>
git checkout <branchname>
```