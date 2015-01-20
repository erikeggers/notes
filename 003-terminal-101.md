- [Introduction to the
  Terminal](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line)
- In many examples, you will see a `$` to signify that you should type the rest
  of the line into the terminal. You do not type the `$`.
- Home (~)
- Up (..)
- Current directory (.)

# Terminal basics
*Note: for the following commands, you do not type the angle brackets, they
indicate a placeholder. You do not type the $ either, that is to indicate you
are on the command line.*

```sh
# make a directory
$ mkdir <directory-name>

# move into a directory
$ cd <directory-name>

# list the contents of a directory
$ ls <directory-name>

# the symbol for the current directory is a dot
$ ls . # this lists the contents of the current directory

# the symbol for the parent directory is ..
$ cd .. # this moves up a directory

# See the current directory
$ pwd

# Create an empty file
$ touch <filename>

# Copy a file
$ cp <filename> <destination>

# Copy a directory
$ cp -R <directory-name> <destination>

# Move or rename a file or directory
$ mv <source> <target>

# Delete a file *Warning: this is not undoable*
$ rm <filename>

# Delete an empty directory
$ rmdir <directory-name>

# Open a file in its default application (This works just like double clicking
# on the icon for the file in Finder)
$ open <filename>

# Open a file in a specific application
$ open -a <ApplicationName.app> <filename>
```
