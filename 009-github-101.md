# Install [hub](https://github.com/github/hub)
hub is a command line tool that lets you interact with GitHub from the CLI.

Install hub via Homebrew by typing `brew install hub` into Terminal.app.

# Creating an SSH key

You'll need an SSH key when using Github. SSH keys are a way to identify trusted
computers, without involving passwords. Walk through the steps in the following
tutorial to create your SSH key and add it to your Github account:
[https://help.github.com/articles/generating-ssh-keys](https://help.github.com/articles/generating-ssh-keys)

## Pushing to GitHub

First you'll need to make a repository on GitHub (replace `<projectname>` with
the name of your project):

```sh
$ hub create <projectname>
```

Or if the repository has already been created on GitHub (replace `<projectname>`
with the name of your project):

```sh
$ hub remote add <projectname>
```

Then, push your commits to GitHub. The first time, you'll need to use:

```sh
$ git push -u origin master
```

After that, you can just use:
```sh
$ git push
```

If you use the wrong command, it might give you an error, but it won't hurt
anything, so don't worry too much about remembering whether you've already
pushed.
