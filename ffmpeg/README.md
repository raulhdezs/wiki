# Overview

Free and open source software to handle video, audio, and other multimedia files and streams.

# Install on Linux:
```bash
sudo apt-get install ffmpeg
```
# Usage examples:
## Create video from file frames
```bash
ffmpeg -framerate 15 -pattern_type glob -i 'frame_*.png' -vf "pad=ceil(iw/2)*2:ceil(ih/2)*2" -vcodec libx264 -pix_fmt yuv420p video.mp4
```
Here the options mean:
- `-framerate 15` A value of 25 is typically used, 15 is still smooth
- `-pattern_type glob` Use expanding shell-like wildcard patterns, e.g. `'frame_*.png'`
- `-i 'frame_*.png'` Input frames
- `-vf [filtergraph]` Create the filtergraph specified by filtergraph and use it to filter the stream.
- `-vf "pad=ceil(iw/2)*2:ceil(ih/2)*2"` Ensure dimensions are even as needed by libx264
- `-vcodec libx264` Set the video codec to libx264 (compatible with QuickTime)
- `-pix_fmt yuv420` Set pixel format
- `-s [width]x[height]` Set frame size

## Cut video
### Specify video duration
```bash
ffmpeg -ss [start] -i in.mp4 -t [duration] -c copy out.mp4
```
### Specify end time
```bash
ffmpeg -ss [start] -i in.mp4 -to [end] -c copy -copyts out.mp4
```

Here the options mean:
- `ss` specifies the start time in seconds, e.g. `00:01:23.000` or `83`
- `t` specifies the duration of the clip
- `to` specifies the end time (needs `-copyts` if `-ss` is before `-i`).
Note that if you've used `-ss`, you have to subtract this from the `-to` timestamp.
For example, if you cut with `-ss 3 -i in.mp4 -to 5`, the output will be five seconds long.
- `c copy` copies the first video, audio, and subtitle bitstream from the input to the output file without re-encoding them. This won't harm the quality and make the command run within seconds.
 
**Source:** https://superuser.com/a/377407
