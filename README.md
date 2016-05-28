# VIM Darcula Theme 1.5

Accurate Darcula color scheme for the VIM editor.  Works well with CoffeeScript projects.  Can be used in 256 color mode.

## What's New?

Updated more accurate colors and additional highlighting.

## What it looks like...

### Using MacVim

![Mac Preview](https://raw.githubusercontent.com/blueshirts/darcula/master/images/darcula1.png)

### Using iTerm2 (256)

![iterm2 Preview](https://raw.githubusercontent.com/blueshirts/darcula/master/images/darcula2.png)

## Installation

### Option 1: Manual installation

1.  Copy darcula.vim into `~/.vim/colors/` (Unix) or `vimfiles/colors/` (Windows).

        $ cd darcula/colors
        $ mv darcula.vim ~/.vim/colors/

### Option 2: Pathogen installation ***(recommended)***


1.  Download and install Tim Pope's [Pathogen](https://github.com/tpope/vim-pathogen).

2.  Next, move or clone the `darcula` directory so that it is 
    a subdirectory of the `.vim/bundle` directory.

    a. **Clone:** 

            $ cd ~/.vim/bundle && \
            git clone git@github.com:blueshirts/darcula.git

    b. **Move:**

        In the parent directory of darcula:
        
            $ mv darcula ~/.vim/bundle/

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
