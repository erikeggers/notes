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

### Resources
- https://try.github.io/
- https://guides.github.com/introduction/flow/
- https://guides.github.com/activities/forking/
- https://help.github.com/articles/github-glossary
- https://help.github.com/articles/what-are-other-good-resources-for-learning-git-and-github

### Setting a repository as upstream remote
This is useful when `origin` points to a fork, you can create a remote for the original repostitory.

Change <repository-url> to the actual URL.

```sh
$ git remote add upstream <repository-url>
```

Then to sync your fork with the original:

```sh
# In your master branch
$ git pull upstream master
$ git push origin master
```

If there are conflicts in your topic branch, you will need to reconcile your branch with the main repository.

```sh
# Fetch the commits from the main repo
$ git fetch upstream
# Merge your current branch with the main's master branch
$ git merge upstream/master
# If there are conflicts between your branch and upstream, they will appear now so that you can fix them.
# Then, you need to add and commit your conflict fixes
$ git add .
# No message necessary, the merge will autofill the message
$ git commit
```

### Modifying a remote URL
This is useful if you accidentally copied the https URL.

```sh
$ git remote set-url upstream <repository-url>
```
