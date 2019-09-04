# VIM Cheat Sheet

## Basic Configs

Installing all plugins thru Vim8 native plugin manager.
No more need for Vundle or Pathogen.

### Ensure version >= 8.0 and and +python3

```
vim --version
```

### Add autocomplete using `TAB`

```
git clone git://github.com/ajh17/VimCompletesMe.git ~/.vim/pack/vendor/start/VimCompletesMe
```

### Add GitGutter

```
git clone git://github.com/airblade/vim-gitgutter.git ~/.vim/pack/vendor/start/gitgutter
```

### Add NERDTree

```
git clone git@github.com:scrooloose/nerdtree.git ~/.vim/pack/vendor/start/nerdtree
```

### Better Low Contrast Colors

```
echo "export TERM=xterm-256color" >> ~/.zshrc

wget https://raw.githubusercontent.com/jnurmine/Zenburn/master/colors/zenburn.vim -O ~/.vim/colors/zenburn.vim
```

### Custom `~/.vimrc` For Plugins Above And Many More

```
set encoding=utf-8
set noswapfile

" Enable line numbers(you can do :set nonumbers to disable)
set nu

" Enable mouse(you can click to go to a place or select with mouse + yy or d
" to copy or delete)
set mouse=a

" Highlight curson line
set cursorline

" Automatically scrolls when cursor gets 10 lines from bottom/top
set scrolloff=10

" Yank copy to copy to clipboard
set clipboard=unnamed

" Display column at 80th character
:set colorcolumn=80

set foldmethod=indent
set foldlevel=99

colors zenburn

let g:gitgutter_async=0
let g:gitgutter_max_signs=9999

" Map F6 to toggle NERDTree (use CTRL + w to swith between tree and file)
nmap <F6> :NERDTreeToggle<CR>
" let NERDTreeIgnore=['\.pyc$', '\~$'] "ignore files in NERDTree
" autocmd vimenter * NERDTree

"------------Start Python PEP 8 stuff----------------
" Number of spaces that a pre-existing tab is equal to.
au BufRead,BufNewFile *py,*pyw,*.c,*.h set tabstop=4

"spaces for indents
au BufRead,BufNewFile *.py,*pyw set shiftwidth=4
au BufRead,BufNewFile *.py,*.pyw set expandtab
au BufRead,BufNewFile *.py set softtabstop=4

" Use the below highlight group when displaying bad whitespace is desired.
highlight BadWhitespace ctermbg=red guibg=red

" Display tabs at the beginning of a line in Python mode as bad.
au BufRead,BufNewFile *.py,*.pyw match BadWhitespace /^\t\+/
" Make trailing whitespace be flagged as bad.
au BufRead,BufNewFile *.py,*.pyw,*.c,*.h match BadWhitespace /\s\+$/

" Wrap text after a certain number of characters
au BufRead,BufNewFile *.py,*.pyw, set textwidth=100

" Use UNIX (\n) line endings.
au BufNewFile *.py,*.pyw,*.c,*.h set fileformat=unix

" Set the default file encoding to UTF-8:
set encoding=utf-8

" For full syntax highlighting:
let python_highlight_all=1
syntax on

" Keep indentation level from previous line:
autocmd FileType python set autoindent

" make backspaces more powerfull
set backspace=indent,eol,start

"Folding based on indentation:
autocmd FileType python set foldmethod=indent
"use space to open folds
nnoremap <space> za 
"----------Stop python PEP 8 stuff--------------


"js stuff"
autocmd FileType javascript setlocal shiftwidth=2 tabstop=2
```

### Case you prefer, use VimRuntime that comes with a lot of stuff

```
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
```

Vim looks for config into `~/.vimrc` but with the VimRuntime plugin that we just installed
it is recommend to add our customizations on `~/.vim_runtime/my_configs.vim`. Sample,
I like to add `set nu` to `~/.vim_runtime/my_configs.vim` to have vim displaying line numbers.


## Basic Commands

`ESC` THEN `w` = navigate forward word by word

`ESC` THEN `W` = navigate forward word by word(consider new word only when whitespace is found)

`ESC` THEN `b` = navigate backward word by word

`ESC` THEN `B` = navigate backward word by word(consider new word only when whitespace is found)

`ESC` THEN `G` = navigate to end of file

`ESC` THEN `gg` = navigate to begin of file

`ESC` THEN `zz` = scroll leaving current line in the middle of screen

`ESC` THEN `zt` = scroll leaving current line in the top of screen

`ESC` THEN `zb` = scroll leaving current line in the bottom of screen

`ESC` THEN `CTRL + U` = scroll up half page at a time

`ESC` THEN `CTRL + D` = scroll down half page at a time

`ESC` THEN `0` = navigate to begin of line

`ESC` THEN `$` = navigate to end of line

`ESC` THEN `H` = navigate to top of current window

`ESC` THEN `M` = navigate to middle of current window

`ESC` THEN `%` = goes to matching brace

`ESC` THEN `i` = enter insert mode at cursor position

`ESC` THEN `I` = enter insert mode at begining of line

`ESC` THEN `a` = enter insert mode after cursor position

`ESC` THEN `A` = enter insert mode at end of line

`ESC` THEN `x` = delete current character

`ESC` THEN `X` = delete previous character

`ESC` THEN `r` = replace current character

`ESC` THEN `dd` = delete current line

`ESC` THEN `gg=G` = auto indent the entire file

`ESC` THEN `:SOME_SUMBER` = go to line SOME_NUMBER

`ESC` THEN `:%s/WORD_TO_FIND/WORD_TO_REPLACE/gc` = find and replace asking for confirmation

## Editing/Commenting/Uncommenting  Multiple Lines

`ESC` THEN `v` =

`ESC` THEN `V` =

`ESC` THEN `CTRL + v` =

