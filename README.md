# VIM Darcula Theme 1.7.3

Accurate Darcula color scheme for the VIM editor.  Works well with CoffeeScript projects.  Can be used in 256 color mode.

## What's New?

Updated the popup colors to be easier on the eyes.

## What it looks like...

### Using MacVim

![Mac Preview](https://raw.githubusercontent.com/blueshirts/darcula/master/images/darcula1.png)

### Using iTerm2 (256)

![iterm2 Preview](https://raw.githubusercontent.com/blueshirts/darcula/master/images/darcula2.png)

## Installation

### Janus: Vim Distribution

Darcula color support has now been added to the Janus Vim Distribution (https://github.com/carlhuda/janus).  Follow the instructions for installing Janus and simply enable syntax highlighting by creating/updating your ~/.vimrc.after file.

.vimrc.after:

    syntax enable
    colorscheme darcula
    
    
### Manual Installation

- Copy darcula.vim into `~/.vim/colors/` (Unix) or `vimfiles/colors/` (Windows).

        $ cp darcula/colors/darcula.vim ~/.vim/colors/

- Update your .vimrc file to enable highlighting.

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

