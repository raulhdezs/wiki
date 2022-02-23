# Overview
A free, open source, and cross-platform media player

## Install on Ubuntu 20.04
```sh
sudo apt update
sudo apt install mpv
```

## How to play multiple videos side-by-side synchronized?
```sh
mpv --lavfi-complex="[vid1][vid2]hstack[vo];[aid1][aid2]amix[ao]" video1.mkv --external-file=video2.mkv
```

Source: https://superuser.com/a/1325668
