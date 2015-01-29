# Ignoring Files in Git

1. Create a file named `.gitignore` horizontal to (i.e. in the same directory as) your git repository. You will need to enable hidden files or use `$ ls -a` to see it.
2. Open `.gitignore` in your text editor.
3. List the files or folders you want git to ignore, one per line.
4. Add and commit the `.gitignore` file to git.
5. (Optional) If you have already committed the files you want to ignore, you will need to tell git to forget about them:

```sh
# Replace `<file-or-folder>` with the name of the file or folder you want git to forget about.
$ git rm --cached <file-or-folder>
```
