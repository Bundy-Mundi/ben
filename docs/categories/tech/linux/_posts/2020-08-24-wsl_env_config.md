---
layout: post
title:  "WSL Environment Configuration"
date:   2020-08-24 9:00:00 +0900
author: Ben Kweon
big_category: tech
---

### A guide for configuring development environment

a. Open your WSL. If you aren’t there, cd to your home directory. The ‘cd’ command with no arguments will take you to your home directory:



b. Create the “C:\\projects” directory from the WSL:

```bash
mkdir /mnt/c/projects
```



c. Create the link to “C:\\projects”. Make sure you are still in your home directory in the WSL and type (if you created ‘projects’ in your windows user home directory, use that path instead):

```bash
ln -s /mnt/c/projects
```



d. This will create a projects directory in your WSL home directory. Verify it points to the Windows directory:

``` bash
ls -l
```



Test that your link works. Create a file in the linked directory with this command:

```bash
touch ~/projects/newfile.txt
```

And verify from your Windows File Explorer that there is a new text file in the C:\\projects\ directory called ‘newfile’.

use

```bash
cd ~/projects
```

to get to the projects directory, and manage all projects in this folder.