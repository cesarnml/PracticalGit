<!-- TOC -->

- [Progress](#progress)
- [Practical Git Commands](#practical-git-commands)
    - [By Trevor Miller](#by-trevor-miller)
  - [Lesson 01 - Lesson 05 - The Basics](#lesson-01---lesson-05---the-basics)
  - [Lesson 06 - Git Branch](#lesson-06---git-branch)
  - [Lesson 07 - Git Merge](#lesson-07---git-merge)
  - [Lesson 08 - Resolving Merge Conflicts](#lesson-08---resolving-merge-conflicts)
  - [Lesson 09 - Git Stash](#lesson-09---git-stash)
  - [Lesson 10 - Git Command Pager](#lesson-10---git-command-pager)
    - [_Less_ commands](#_less_-commands)
  - [Lesson 11 - Git Log](#lesson-11---git-log)
  - [Lesson 12 - Format Git Log](#lesson-12---format-git-log)
  - [Lesson 13 - Filter Git Log](#lesson-13---filter-git-log)
  - [Lesson 14 - Git Diff](#lesson-14---git-diff)
  - [Lesson 15 - Git Blame](#lesson-15---git-blame)
  - [Lesson 16 - Git Tag](#lesson-16---git-tag)
  - [Lesson 17 - Git Rebase](#lesson-17---git-rebase)
  - [Lesson 18 - Git Bisect - Huntdown Bad Commits](#lesson-18---git-bisect---huntdown-bad-commits)
  - [Lesson 19 - Git Hooks](#lesson-19---git-hooks)
  - [Lesson 20 - ~/.gitconfig](#lesson-20---gitconfig)
  - [Lesson 21 - .gitignore](#lesson-21---gitignore)
  - [Lesson 22 - Global .gitignore](#lesson-22---global-gitignore)

<!-- /TOC -->
## Progress
* [x] Lesson 01
* [x] Lesson 02
* [x] Lesson 03
* [x] Lesson 04
* [x] Lesson 05
* [x] Lesson 06
* [X] Lesson 07
* [X] Lesson 08
* [X] Lesson 09
* [X] Lesson 10
* [X] Lesson 11
* [X] Lesson 12
* [X] Lesson 13
* [X] Lesson 14
* [x] Lesson 15
* [x] Lesson 16
* [x] Lesson 17
* [x] Lesson 18
* [x] Lesson 19
* [x] Lesson 20
* [x] Lesson 21
* [x] Lesson 22

## Practical Git Commands
#### By Trevor Miller

### Lesson 01 - Lesson 05 - The Basics
`git init` => init a git dir

`git clone` => clone remote git dir to local

`git status` => report current status of local git repo

`git add -A` => track all changed files

`git commit -m` => stage all modified tracked files

`git push` => push local changes to remote repo

```bash
git add -A
git commit -m
git push
```

`git pull` => `git fetch` + `git merge`

### Lesson 06 - Git Branch
`git branch` => list all branches

`git branch [name]` => create a new branch

`git checkout [name]` => make active branch

`git checkout -b [name]` => creates and checks-out new branch

`git checkout -` => switches to previously checked out branch

_NOTE: I need to start making better use of git branches._

### Lesson 07 - Git Merge

`git merge [branch]` => merge desired branch to current checkout branch

`git branch -d [branch]` => delete a branch (e.g after successful merge)

### Lesson 08 - Resolving Merge Conflicts

**HEAD** your conflicting changes

**===** dividing line separating conflicts

**>>>>** remote repo changes

1. Run `git status` to determine which files have a conflict
2. Resolve conflict in favorite text editor
3. Run `git add -A, git commit -m, git push`

### Lesson 09 - Git Stash
 `git stash` => run after `git add -A` to stash changes that aren't ready for a full commit

 `git stash apply` => reapply stashed changes

### Lesson 10 - Git Command Pager
`git log` likely to open up in a pager (e.g _less_)

#### _Less_ commands
`j` one line down

`k` one like up

`^f` page forward

`^b` page backward

`/[search]` search for a term

`n` next search match

`N` previous search match

`q` quit pages (e.g. _less_)

### Lesson 11 - Git Log
`git log` view commit history

`git log [arg]` format git log with arg

### Lesson 12 - Format Git Log
`git log --oneline` short log, commit ID & message

`git log --decorate` shows all refs

`git log --graph` visualize branches/mergers 

`git log -p` patch, shows changes made in each commit

`git log --stat` gives an edit summary for each commit

### Lesson 13 - Filter Git Log
 `git log -n` show last n commits
 
 `git log --after` show commits after date (e.g _'yesterday'_, _'3/15/18'_, _'last tuesday'_, _'30 minutes ago'_)

`git --before`, `git --since`, `git --until` => all work similar

`git log --author` => search for authors

`git log --grep="string"` => filter by string

`git log -p -S"Math"` => find commits with Math string changed - **pick axe method**

`git log -p -GMath` => regex search of commits

`git log -i` => ignore case option

`git log --no-merges` => don't show merge commits

`git log [filename]` => will show file specific logs

**Most of these commands are composable**

### Lesson 14 - Git Diff
`git diff` => Changes between last commit and current working directory

`git diff origin/master` => compare local to remote origin/master

`git diff --cached` => compare staged changes to locally saved changes

`git diff [filename]` => limits diff to specified file

### Lesson 15 - Git Blame
`git blame [filename]` => last person to edit line 

### Lesson 16 - Git Tag
`git tag` => to create a reference to a commit that can't be changed 
  - usually used for semantic versioning v1.0.0 Major.Minor.Patch)

### Lesson 17 - Git Rebase
`git rebase` => used to combine commit messages; use with caution

`git squash` =>  used to combine several commits into a single commit

_NOTE: this section was bit confusing, return to later._

### Lesson 18 - Git Bisect - Huntdown Bad Commits
`git bisect start` => begin a bisecting state

`git bisect bad` => mark current commit as bad

`git bisect good [GitID]` => sets commit to good

_NOTE: Advance feature. Return later._

### Lesson 19 - Git Hooks
- Git Hooks
  - pre-commit
  - pre-rebase
  - post-commit
  - post-merge
  - post-checkout

### Lesson 20 - ~/.gitconfig
`git config --global` => edits the global .gitconfig file

### Lesson 21 - .gitignore
- Files we might need to ignore:
  - .DS_Store (Mac Finder)
  - `git rm --cached` 
  - Thumbs.db (Windows)
  - node_modules (npm)
  - npm-debug.log (npm)
  - *.png
  - cache

### Lesson 22 - Global .gitignore
`git config --global core.excludesfile ~/.gitignore_global` => setup global .gitignore file
