# Commit often
If you commit often, you're able to easily throw away your changes without fear.

## Warning: this command is irrecoverable
To discard, forever and without recovery, your changes in your working directory.

```sh
$ git checkout -- .
```
## pretty log

```sh
$ git config --global format.pretty "%C(yellow)%h%Creset %s %C(red)(%an, %cr)%Creset"
$ git config --global core.pager "less -FRSX"
```

## tig (a nicer looking git CLI)
```sh
$ brew install tig
```

## Overview
- Commits are created with `git commit`
- Branches are just labels for commits
- "Merging branches" means merging the histories of commits that two branches point at.
- Most git commands operate on where HEAD is pointed
- `git pull` is just `git fetch` and `git merge` in one command. It pulls in the history from the remote, and then merges it into HEAD.

## Creating a branch

```sh
$ git checkout -b <branchname>
```

## Merging a branch
To merge a branch INTO master

```sh
$ git checkout master
$ git merge <branchname>
```

### Resources
- https://try.github.io/
- https://help.github.com/articles/github-glossary
- https://help.github.com/articles/what-are-other-good-resources-for-learning-git-and-github
