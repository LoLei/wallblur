# wallblur

wallblur is a simple shell script that creates a faux blurred background effect for your linux desktop without needing a compositor.

![demo](https://github.com/turing753/wallblur/blob/master/demo.gif)

## Getting Started

### Dependencies

In order to use the script, you will need to make sure you have imagemagick, feh and wmctrl installed.

If not, you can do so by executing:

```
sudo apt install imagemagick wmctrl feh
```

### pywal Users

If you are a pywal user, you might want to use the "wallblur.sh" script. It will automatically read your current wallpaper from the pywal cache.

### non-pywal Users

If you do not use pywal, you need to use the "wallblur_nopywal.sh" script. To configure it for your current wallpaper, change the ***Pictures/Wallpapers/samuraijack.jpg*** part in the following line to your current wallpaper.

```
curr_wallpaper="/home/"$curr_user"/Pictures/Wallpapers/samuraijack.jpg"
```

### Note

Make sure that you stop any existing application that is responsible for setting your wallpaper.


## Running wallblur

You can run wallblur by running the following command:

```
path/to/wallblur.sh &
```

If you would like to start wallblur on startup automatically, assuming you are on an X11 windowing system, add the following line to your **.xprofile** file:

```
path/to/wallblur.sh &
```

Replacing ***path/to/*** with the actual path where the script is residing.

If you are using **i3wm**, you can add this line to your config:

```
exec --no-startup-id sh -c "path/to/wallblur.sh &"
```


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details