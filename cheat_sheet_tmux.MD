# TMUX Cheat Sheet

`apt install tmux` OR `brew install tmux` = seriously!?

`~/.tmux.conf` = config file for tmux

## Basic Conf

Based on https://thoughtbot.com/blog/how-to-copy-and-paste-with-tmux-on-mac-os-x

# Based on https://www.rushiagr.com/blog/2016/06/16/everything-you-need-to-know-about-tmux-copy-pasting-ubuntu/

## Basic Commands

`tmux` = start tmux in a new session

`CTRL + b` THEN `%` = split pane into left and right

`CTRL + b` THEN `"` = split pane into top and bottom

`CTRL + b` THEN `ARROW_KEYS` = navigate thru panes

`CTRL + b` THEN `z` = toggle pane fullscreen

`CTRL + b` THEN `ALT + ARROW_KEYS` = resize current pane

`exit` OR `CTRL + d` = close pane

`CTRL + b` THEN `c` = create new window(all windows displayed left side of tmux status bar)

`CTRL + b` THEN `p` = loop thru windows

`CTRL + b` THEN `WINDOW_NUMBER` = go to specific window number

`CTRL + b` THEN `d` = detach session

`tmux ls` = list detached sessions

`tmux attach -t SESSION_NUMBER OR SESSION_NAME` = connect to tmux sesion specified

`tmux new -s SESSION_NAME` = start new tmux session with a name

`tmux rename-session -t 0 SESSION_NAME` = rename session 0 to SESSION_NAME

`CTRL + b` THEN `[` THEN `ARROW_KEYS` = to scroll thru a tmux pane then press `q` to stop scrolling. Or add `set -g mouse on` to `~/.tmux.conf` to enable mouse scroll/pane switching
