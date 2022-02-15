# Personal wiki

## Table of contents
1. [Overview](#overview)  
2. [Useful commands](#commands)  
3. [Packages](#packages)  
4. [License](#license)  

<a name="overview"/>

## Overview

Here I try to document everything I learn using Ubuntu.

<a name="commands"/>

## Useful commands
### date
- Description: Print or set the system date and time
- Example of use: Print current date in YYYY-MM-DD format
```sh
date +%Y-%m-%d
```
### mkdir
- Description: Make directories
- Example of use: Make directory including date
```sh
mkdir $(date +%Y-%m-%d)_directory-name
```

<a name="packages"/>

## Packages

### htop
- Description: Free and open source ncurses-based process viewer (i.e. to see what's happening with your computer resources).
- Install:
```sh
$ sudo apt-get install htop
```
### tree
- Install:
```sh
$ sudo apt-get install tree
```

### fd
- Description: Program to find entries in the filesystem.
- Install:
```sh
sudo apt-get install fd-find
ln -s $(which fdfind) ~/.local/bin/fd
```


### kazam
- Description: Simple screen recording program.
- Install:
```bash
sudo apt-get install kazam
```

### Homebrew
- Description: Package manager.
- Install
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### tldr
- Description: Simplified man pages

<a name="license"/>

## License

Distributed under the MIT License. See `LICENSE` for more information.

**Disclaimer:** All the contents given in this repository are provided "as-is" without any guarantee on the impact on your system/code. 
Be aware that using anything in these notes is only based on your responsability.
