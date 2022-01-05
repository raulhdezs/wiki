# Overview
Tmux is a terminal multiplexer. It lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal.

## Install
```sh
$ sudo apt-get insall tmux
```

## Panes
### Splitting panes
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>%</kbd> &nbsp; Split into left and right panes
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>"</kbd> &nbsp; Split into top and bottom panes
### Navigating panes
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>arrow key</kbd>
### Closing panes
- <kbd>Ctrl</kbd>+<kbd>d</kbd> &nbsp; or type ```exit```
### Resize pane
- <kbd>Ctrl</kbd>+<kbd>d</kbd> &nbsp; <kbd>Ctrl</kbd>+<kbd>arrow key</kbd>
### Full screen
- <kbd>Ctrl</kbd>+<kbd>d</kbd> &nbsp; <kbd>z</kbd> &nbsp; Go full screen
- <kbd>Ctrl</kbd>+<kbd>d</kbd> &nbsp; <kbd>Z</kbd> &nbsp; Shrink it back to its previous size

## Windows
### Creating a new window
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>c</kbd>
### Navigating windows
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>p</kbd> &nbsp; Switch to *previous* window
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>n</kbd> &nbsp; Switch to *next* window
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>number</kbd> &nbsp; Switch to window *number* (the status bar will tell you which window has which number)
### Rename window
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>,</kbd>


## Sessions
### Detaching
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>d</kbd> &nbsp; Detach your current session
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>D</kbd> &nbsp; Choose the session to detach
### List all running sessions
Type ```tmux ls```
### Attach running session
Type ```tmux attach -t <session name>```
### Name sessions
- Type ```tmux new -s <session name>``` to create a new session with the name of your choice.
- Type ```tmux rename-session -t <old session name> <new session name>``` to rename a running session.
### More available commands
- <kbd>Ctrl</kbd>+<kbd>b</kbd> &nbsp; <kbd>?</kbd>


**Reference:** [A Quick and Easy Guide to tmux by Ham Vocke](https://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/)

## How to keep processes running after ending ssh session?
1. ssh into the remote machine
2. start tmux by typing ```tmux``` into the shell
3. start the process you want inside the started tmux session
4. detach the tmux session by typing <kbd>Ctrl</kbd>+<kbd>b</kbd> and then <kbd>d</kbd>
5. type ```tmux ls``` into the shell to get a list of the currently running sessions
6. type ```tmux attach-session -t <session-name>``` to attach to a runinng session
 
**Reference:** [StackOverflow: How to keep processes running after ending ssh session?](https://askubuntu.com/questions/8653/how-to-keep-processes-running-after-ending-ssh-session)
