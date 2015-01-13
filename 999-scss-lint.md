# SCSS Lint
## Install the CLI tool
```sh
$ gem install scss-lint
# or
$ sudo gem install scss-lint
```

## Downloading the configuration file
*This will download the configuration file into your home directory*

```sh
$ curl https://raw.githubusercontent.com/jacobthemyth/dotfiles/master/scss-lint.yml > ~/.scss-lint.yml
```

## Using scss-lint in Atom

1. You must already have the CLI tool and the Linter package installed.
2. Install the package named linter-scss-lint.
3. Go to the Settings page for linter-scss-lint.
4. Delete the contents of the Excluded Linters box (if it exists) so that Atom
   uses the configuration file you installed above.
