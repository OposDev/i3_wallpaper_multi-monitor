# i3-video-wallpaper
Play dynamic wallpapers in i3wm (using XWinWrap and MPV).

- Support pausing the video when a window other than the desktop is focused
- Multi-monitor support
- Set FPS for videos

## Dependencies
- xwinwrap
- xdotool
- mpv

## Optional Dependencies
- ffmpeg (to generate thumbnail)
- feh (to set wallpaper)
- imagemagick (to blur the generated thumbnail)

## Basic Usage
```bash
./setup.sh [-a false] [-r] [-m] [-p] [-n false] [-w false] [-b false] [-g 16x16] [-f center] [-d $HOME/Pictures/i3-video-wallpaper] [-t 00:00:01] [-h]
```
## Parameters
```
$ ./setup.sh -h
Options:
        -a: Always run video wallpaper. (Default: false)
        -r: Path to video 1.
        -m: Path to video 2.
        -p: Path to video 3.
        -s: FPS (Default 40).
        -n: Generate a thumbnail by using ffmpeg. It can fix the background of system tray if you use the built-in system tray of Polybar. (Default: false)
        -w: Set the generated thumbnail as wallpaper by using feh. It can fix the background of system tray if you use the built-in system tray of Polybar. (Default: false)
        -b: Blur the thumbnail. It may be useful if your compositor does not blur the background of the built-in system tray of Polybar. (Default: false)
        -g: Parameter which is passed to "convert -blur [parameter]". (Default: 16x16)
        -f: Parameter which is passed to "feh --bg-[paramater]". Available options: center|fill|max|scale|tile (Default: center)
        -d: Where the thumbnails is stored. (Default: $HOME/Pictures/i3-video-wallpaper)
        -t: The time to generate the thumbnail. (Default: 00:00:01) 
        -h: Display this text.
```
## Edit number of monitors
- Add/remove getopts args.
- Edit line 135 depending on number of monitors.


## License
[MIT](https://mit-license.org)

## References
- [How to get an animated background on linux like mine and understanding PID files.](https://www.youtube.com/watch?v=b8rh9m3wOjk&list=PLRtT6Oib2tb2HrWb3gfUWdE4S21802mVF&index=1&t=901s)
