# Bourbon and Neat
## Installing the CLI tools
```sh
# The square brackets indicate an optional segment of the command
$ [sudo] gem install bourbon
$ [sudo] gem install neat
```

## Install the Bourbon and Neat files into your project
**Note: you must be in your project directory when you use these commands**

```sh
# replace 'styles' with the name of the directory where your styles are
$ cd styles
$ bourbon install
$ neat install
```

Then, in your main stylesheet:

```scss
@import 'bourbon/bourbon';
@import 'neat/neat';
```
