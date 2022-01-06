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
- Description: Free and open source ncurses-based process viewer
- Install:
```sh
$ sudo apt-get install htop
```
### tree
- Install:
```sh
$ sudo apt-get install tree
```

### ffmpeg
- Description: Free and open source software to handle video, audio, and other multimedia files and streams.
- Install:
```sh
$ sudo apt-get install ffmpeg
```
- Usage:
  - Create video from file frames:
```sh
$ ffmpeg -framerate 25 -pattern_type glob -i 'frame_*.png' -c:v libx264 -crf 20 -pix_fmt yuv420p -vcodec mpeg4 video.mp4
```

## License

Distributed under the MIT License. See `LICENSE` for more information.

**Disclaimer:** All the contents given in this repository are provided "as-is" without any guarantee on the impact on your system/code. 
Be aware that using anything in these notes is only based on your responsability.
