# VIM Darcula Theme 1.7

Accurate Darcula color scheme for the VIM editor.  Works well with CoffeeScript projects.  Can be used in 256 color mode.

## What's New?

Updated the popup colors to be easier on the eyes.

## What it looks like...

### Using MacVim

![Mac Preview](https://raw.githubusercontent.com/blueshirts/darcula/master/images/darcula1.png)

### Using iTerm2 (256)

![iterm2 Preview](https://raw.githubusercontent.com/blueshirts/darcula/master/images/darcula2.png)

## Installation

- Copy darcula.vim into `~/.vim/colors/` (Unix) or `vimfiles/colors/` (Windows).

        $ cp darcula/colors/darcula.vim ~/.vim/colors/

### Modify .vimrc

After either Option 1 or Option 2 above, put the following two lines in your
.vimrc:

    syntax enable
    colorscheme darcula

## CoffeeScript Configuration

Add the following content to the `.vim/after/syntax/coffee/coffee.vim` file.  This configuration is required with most
VIM CoffeeScript syntax highlighters in order to properly color the '@' (this) symbol.

    hi clear coffeeParens
    hi coffeeParens NONE
    syn clear coffeeParens

    hi clear coffeeSpecialIdent
    hi coffeeSpecialIdent NONE
    syn clear coffeeSpecialIdent

    hi clear coffeeCurlies
    hi coffeeCoffeeCurlies NONE
    syn clear coffeeCurlies

    " Highlight the this symbol.
    syn match coffeeThis "\v\@"
    hi def link coffeeThis Keyword

