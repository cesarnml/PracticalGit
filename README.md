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

<!-- /TOC -->
# Progress
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
* [ ] Lesson 11
* [ ] Lesson 12
* [ ] Lesson 13
* [ ] Lesson 14
* [ ] Lesson 15
* [ ] Lesson 16
* [ ] Lesson 17
* [ ] Lesson 18
* [ ] Lesson 19
* [ ] Lesson 20
* [ ] Lesson 21
* [ ] Lesson 22

# Practical Git Commands
#### By Trevor Miller

## Lesson 01 - Lesson 05 - The Basics
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

## Lesson 06 - Git Branch

`git branch` => list all branches

`git branch [name]` => create a new branch

`git checkout [name]` => make active branch

`git checkout -b [name]` => creates and checks-out new branch

`git checkout -` => switches to previously checked out branch

_NOTE: I need to start making better use of git branches_

## Lesson 07 - Git Merge

`git merge [branch]` => merge desired branch to current checkout branch

`git branch -d [branch]` => delete a branch (e.g after successful merge)

## Lesson 08 - Resolving Merge Conflicts

**HEAD** your conflicting changes

**===** dividing line separating conflicts

**>>>>** remote repo changes

1. Run `git status` to determine which files have a conflict
2. Resolve conflict in favorite text editor
3. Run `git add -A, git commit -m, git push`

## Lesson 09 - Git Stash
 `git stash` => run after `git add -A` to stash changes that aren't ready for a full commit

 `git stash apply` => reapply stashed changes

## Lesson 10 - Git Command Pager
`git log` likely to open up in a pager (e.g _less_)
### _Less_ commands
`j` one line down

`k` one like up

`^f` page forward

`^b` page backward

`/[search]` search for a term

`n` next search match

`N` previous search match

`q` quit pages (e.g. _less_)

## Lesson 11 - Git Log
`git log` view commit history

`git log [arg]` format git log with arg

## Lesson 12 - Format Git Log
`git log --oneline` short log, commit ID & message

`git log --decorate` shows all refs

`git log --graph` visualize branches/mergers 

`git log -p` patch, shows changes made in each commit

`git log --stat` gives an edit summary for each commit

## Lesson 13 - Filter Git Log

