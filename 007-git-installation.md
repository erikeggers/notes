# Git 101
Git is a computer program that you interact with via the command line. It is
used to track changes to your files over time. It is very important to
understand that git and GitHub are two separate things. git is an open source
change tracking program, GitHub is a company and an online service that allows
you to collaborate on programming projects using git as the backbone of its
service.

## Install git
**Prerequisite: Install Homebrew**
To install git, simply issue the following command on the command line, which is
telling homebrew to download and install the git program:

*Note: you should not type the `$` symbol, that is simply used to indicate that
you are supposed to type the command on the command line*

```sh
$ brew install git
```

To make sure that worked, you can ask git to tell you its version:

```sh
$ git --version
```

Which should print out something that looks like the following (anything greater
than 1.8 is fine).

```sh
git version 2.2.1
```

## Configure git
It is **crucial** that you configure git with the email address that is
associated with your GitHub account. If you are not sure, check, then double
check.

What this command does is tell git that, when you track changes to your files,
those changes should be associated with you.

```sh
# Lines in shell examples that start with a `#` mark are comments, by the way
# You shouldn't type them, they just give you information
# Replace <Your email> with... your email!
$ git config --global user.email "<Your email>"
```

```sh
# Replace <Your name> with... your name!
$ git config --global user.name "<Your name>"
```

You probably want to also tell git to use Atom as its default editor, otherwise
it will open vim, an arcane command line text editor.

```sh
$ git config --global core.editor "atom --wait"
```
