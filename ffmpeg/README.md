# Overview

Free and open source software to handle video, audio, and other multimedia files and streams.

# Install on Linux:
```bash
sudo apt-get install ffmpeg
```
# Usage examples:
## Create video from file frames
```bash
ffmpeg -framerate 25 -pattern_type glob -i 'frame_*.png' -c:v libx264 -crf 20 -pix_fmt yuv420p -vcodec mpeg4 video.mp4
```
## Cut video
### Specify video duration
```bash
ffmpeg -ss [start] -i in.mp4 -t [duration] -c copy out.mp4
```
### Specify end time
```bash
ffmpeg -ss [start] -i in.mp4 -to [end] -c copy -copyts out.mp4
```

Here the options mean the following:
- `ss` specifies the start time in seconds, e.g. `00:01:23.000` or `83`
- `t` specifies the duration of the clip
- `to` specifies the end time (needs `-copyts` if `-ss` is before `-i`).
Note that if you've used `-ss`, you have to subtract this from the `-to` timestamp.
For example, if you cut with `-ss 3 -i in.mp4 -to 5`, the output will be five seconds long.
- `c copy` copies the first video, audio, and subtitle bitstream from the input to the output file without re-encoding them. This won't harm the quality and make the command run within seconds.
 
**Source:** https://superuser.com/a/377407
