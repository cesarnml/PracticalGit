<!-- TOC -->

- [Practical Git Commands](#practical-git-commands)
      - [By Trevor Miller](#by-trevor-miller)
  - [Progress](#progress)
  - [Lesson 01 - Lesson 05 - The Basics](#lesson-01---lesson-05---the-basics)
  - [Lesson 06 - Git Branch](#lesson-06---git-branch)
  - [Lesson 07 - Git Merge](#lesson-07---git-merge)
  - [Lesson 08 - Resolving Merge Conflicts](#lesson-08---resolving-merge-conflicts)

<!-- /TOC -->

# Practical Git Commands
#### By Trevor Miller

## Progress
* [x] Lesson 01
* [x] Lesson 02
* [x] Lesson 03
* [x] Lesson 04
* [x] Lesson 05
* [x] Lesson 06
* [X] Lesson 07
* [ ] Lesson 08
* [ ] Lesson 09
* [ ] Lesson 10
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

## Lesson 07 - Git Merge

`git merge [branch]` => merge desired branch to current checkout branch

`git branch -d [branch]` => delete a branch (e.g after successful merge)

## Lesson 08 - Resolving Merge Conflicts


