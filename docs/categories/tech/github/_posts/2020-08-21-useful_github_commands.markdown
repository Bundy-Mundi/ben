---
layout: post
title:  "Useful Githiub Commands"
date:   2020-08-20 12:00:00 +0900
author: Ben Kweon
big_category: tech
sub_category: github
---

### 1. Switch Branch

1. Pull the changes from upstream.
```bash
$ git pull
```

2. Create a branch
```bash
$ git checkout -b [name_of_your_new_branch]
```

3. Push the branch
```bash
$ git push origin [name_of_your_new_branch]
```

### 2. Delete a Branch
```bash
$ git push [remote_url] :[name_of_your_new_branch]
```
Also,
```bash
$ git push [remote_url] --delete [name_of_your_new_branch]
```

### 3. See All Branches

```bash
$ git branch -a
```

### 4. List All Remote URLs
```bash
$ git remote -v
``` 

### 5. Change Remote URL
```bash
$ git remote set-url origin [name_of_your_new_url]
```

### 6. Synchronize Branch List





