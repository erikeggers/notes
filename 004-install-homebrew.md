# [XCode](https://developer.apple.com/xcode/)

Xcode is an integrated development environment (IDE) containing a suite of
software development tools developed by Apple for developing software for OS X
and iOS.

You are welcome to install XCode.app through the Mac App Store, but it is quite
large and all we actually need are the Command-Line Tools. If you want to save
some hard drive space, you can install just the part we need:

1.  Open Terminal.app (Applications &gt; Utilities &gt; Terminal)
2.  Copy (or type) the following into the terminal, then press `return`:

    ```sh
    xcode-select --install
    ```

3. A window will appear saying “The xcode-select command requires the command
   line developer tools. Would you like to install the tools now?”. Follow the
   instructions to install the tools.

**Note:** If you see the error “Can’t install the software because it is not
currently available from the Software Update server”, it means you probably
already have the tools installed

# [Homebrew](http://brew.sh/)

Homebrew is a package manager for installing development tools onto your Apple
computer. It's sort of like the app store for developers.

1.  Open Terminal.app (Applications &gt; Utilities &gt; Terminal)
2.  Copy (or type) the following into the terminal, then press `return`:

    ```sh
    ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
    ```

3.  Follow the instructions on-screen.
4.  When finished, run `brew doctor`.

