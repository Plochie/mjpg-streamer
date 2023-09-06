mjpg-streamer
=============

This is a fork of http://sourceforge.net/projects/mjpg-streamer/ with added support for the Raspberry Pi camera via the input_raspicam plugin.

Security warning
----------------

**WARNING**: mjpg-streamer should not be used on untrusted networks!
By default, anyone with access to the network that mjpg-streamer is running
on will be able to access it.

Building & Installation
=======================

You must have cmake installed. You will also probably want to have a development
version of libjpeg installed. I used libjpeg8-dev. e.g.

    sudo apt-get install cmake libjpeg62-turbo-dev
    sudo apt-get install gcc g++


Simple compilation
------------------

This will build and install all plugins that can be compiled.

    cd mjpg-streamer-experimental
    make all
    sudo make install

Usage
=====
From the mjpeg streamer experimental
folder:
```
mjpg_streamer -o "output_http.so -w ./www" -i "input_uvc.so --resolution SXGA"
```

See [README.md](mjpg-streamer-experimental/README.md) or the individual plugin's documentation for more details.

