# VIM Darcula Theme

Accurate Darcula color scheme for the VIM editor.  Works well with CoffeeScript projects.  Can be used in 256 color mode.

## What it looks like...

### Using MacVim

![Mac Preview](https://raw.githubusercontent.com/blueshirts/darcula/master/images/darcula1.png)

### Using iTerm2 (256)

![iterm2 Preview](https://raw.githubusercontent.com/blueshirts/darcula/master/images/darcula2.png)

## Installation

Copy darcula.vim into `~/.vim/colors/` (Unix) or `vimfiles/colors/` (Windows).

Type `"colorscheme railscasts"` into your vimrc file.

## CoffeeScript Configuration

Add the following content to the `.vim/after/syntax/coffee/coffe.vim` file.  This configuration is required with most
VIM CoffeeScript syntax highlighters in order to properly color the '@' (this) symbol.

    " Highlight the this symbol.
    syn match coffeeThis "\v\@"
    hi def link coffeeThis Keyword