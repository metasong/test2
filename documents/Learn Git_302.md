# Learn Git
---
author: Jason Song <metaseed@gmail.com>
version: 1.0.0
tag: []
enable: [toc]
---
http://gitready.com

https://blog.osteele.com/2008/05/my-git-workflow/

http://onlywei.github.io/explain-git-with-d3/#commit

https://marklodato.github.io/visual-git-guide/index-en.html

http://ndpsoftware.com/git-cheatsheet.html
http://justinhileman.info/article/git-pretty/git-pretty.png
https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf
https://github.com/git/git/blob/master/Documentation/howto/revert-a-faulty-merge.txt

## Diagrams

![](https://marklodato.github.io/visual-git-guide/basic-usage.svg)
* git reset -- files copies files from the latest commit to the stage. Use this command to "undo" a git add files. 
* git checkout -- files copies files from the stage to the working directory. Use this to throw away local changes.
* You can use git reset -p or --patch, git checkout -p, or git add -p instead of (or in addition to) specifying particular files to interactively choose which hunks copy.

![](https://marklodato.github.io/visual-git-guide/basic-usage-2.svg)

## help
* `git help add` open online help
* `git add -h` show help in console

## file status
![](https://git-scm.com/book/en/v2/images/lifecycle.png)
`git add` is used to stage changes for next commit.
## workflow
![=80%x](https://i.stack.imgur.com/MgaV9.png)

* `git add -u` is update tracked files, untracked file(newly added file) is not included.
* The `git add` command can be used to add ignored files with the -f (force) option

The index is a mechanism for preventing what you commit from matching what you tested in your working directory

The Index is the staging area in git. It’s basically a layer that separates your working tree from the Git repository. This gives developers more power over what gets sent to the Git repository.

HEAD is a pointer that points to the current branch. A repository only has 1 active HEAD.
head is a pointer that points to any commit. A repository can have any number of heads.

![](https://images.osteele.com/2008/git-workflow.png)

This way I can checkpoint every few minutes. It’s a very cheap operation, and I don’t have to spend time cleaning up the checkpoints later. `git diff` tells me what I’ve changed since the last checkpoint; `git diff head` shows what’s changed since the last commit. `git checkout .` reverts to the last checkpoint; `git checkout head .` reverts to the last commit. And `git stash` and `git checkout -m -b` operate on the changes since the last 

https://git-scm.com/book/en/v2/Git-Internals-Git-Objects

commit, which is what I want.