# Install [Node](http://nodejs.org/)

Node.js is a platform built on Chrome's JavaScript runtime for easily building
fast, scalable network applications. Node.js uses an event-driven, non-blocking
I/O model that makes it lightweight and efficient, perfect for data-intensive
real-time applications that run across distributed devices.

Install node.js via Homebrew by typing `brew install node` into Terminal.app.

If you already installed node, you will likely get permissions errors. It is
usually fine to obliterate node and start over, which can be done using the
following command, but beware, it is destructive and could result in loss of
data if you are not careful.

```sh
$ bash -c "$(curl -fsSL https://gist.githubusercontent.com/jacobthemyth/8a1316bd064ca83c2c2d/raw/d9e922fa195dded8436cf3a35998ec4ce2b7309c/nukenode.sh)"
```

