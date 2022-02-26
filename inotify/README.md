# Overview
`inotify-tools` is a C library and a set of command-line programs for Linux providing a simple interface to inotify.
These programs can be used to monitor and act upon filesystem events.

## Install
```sh
sudo apt install inotify-tools
```

## Commands
- `inotifywait` This command simply blocks for inotify events, making it appropriate for use in shell scripts. It can watch any set of files and directories, and can recursively watch entire directory trees.

### Usage example
- How to keep two folders automatically synchronized
```sh
while inotifywait -r -e modify,create,delete,move dir_source; do
    rsync -avz dir_source dir_destination
done
```
Source: https://github.com/inotify-tools/inotify-tools/wiki
