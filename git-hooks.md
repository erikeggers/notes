## Git hooks

To make sure your bower and npm packages are always up to date, you can use the following hooks to run the commands when you checkout or merge a branch.

Create a file .git/hooks/post-checkout
Create a file .git/hooks/post-merge

The contents of both should be:

```sh
#!/bin/sh
[ -f package.json ] && npm install > /dev/null &
[ -f bower.json ] && bower update > /dev/null &
```

Then run the following commands:

```sh
$ chmod 755 .git/hooks/post-checkout
$ chmod 755 .git/hooks/post-merge
```

