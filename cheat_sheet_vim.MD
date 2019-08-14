# VIM Cheat Sheet

## Basic Configs

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

`ESC` THEN `i` = enter insert mode at cursor position

`ESC` THEN `I` = enter insert mode at begining of line

`ESC` THEN `a` = enter insert mode after cursor position

`ESC` THEN `A` = enter insert mode at end of line

`ESC` THEN `x` = delete current character

`ESC` THEN `X` = delete previous character

`ESC` THEN `r` = replace current character

`ESC` THEN `dd` = delete current line

`ESC` THEN `:$` = go to last line

`ESC` THEN `:SOME_SUMBER` = go to line SOME_NUMBER

`ESC` THEN `:%s/WORD_TO_FIND/WORD_TO_REPLACE/gc` = find and replace asking for confirmation

## Editing/Commenting/Uncommenting  Multiple Lines

`ESC` THEN `v` =

`ESC` THEN `V` =

`ESC` THEN `CTRL + v` =

