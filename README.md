# Personal wiki

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#overview">Overview</a>
    </li>
    <li>
      <a href="#license">License</a>
    </li>
  </ol>
</details>

## Overview

Here I try to document the solutions to software issues I face as well as interesting utilities.

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

## License

Distributed under the MIT License. See `LICENSE` for more information.

**Disclaimer:** All the contents given in this repository are provided "as-is" without any guarantee on the impact on your system/code. 
Be aware that using anything in these notes is only based on your responsability.
