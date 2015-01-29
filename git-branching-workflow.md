## The basic git workflow with branches

```sh
$ git init
# Create files
$ (master) git add .
$ (master) git commit -m "Initial commit"
$ (master) git push -u origin master
$ (master) git checkout -b my-branch
$ (my-branch) git status
# Now when you make commits they will be on your branch
$ (my-branch) git add .
$ (my-branch) git commit -m "Cool changes"
$ (my-branch) git checkout master
$ (master) git merge my-branch
$ (master) git push
```
