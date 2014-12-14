---
title: media-autobuild_suite

description: A Windows automatic build script for ffmpeg and other media tools

author: Jonathan Baecker (jb_alvarado)

tweaked by: Matt Bunce (mjb2000)

created:  2013-09-24

modified: 2014-12-08

tweaked: 2014-12-14

---

media-autobuild_suite
=========

This tool is based on the original script from [jb-alvarado](https://github.com/jb-alvarado/media-autobuild_suite).

I have tweaked the script to fix a couple of issues and use a couple of private forked versions of [mfx_dispatcher](https://github.com/mjb2000/mfx_dispatch) and [ffmpeg](https://github.com/mjb2000/FFmpeg) to build ffmpeg with Intel QuickSync support

jb-alvarado's tool was inspired by the very nice, linux cross compile, tool from Roger Pack(rdp):
https://github.com/rdp/ffmpeg-windows-build-helpers

It is based on msys2 and tested under Windows 7.
http://sourceforge.net/projects/msys2/

I use some jscipt parts from nu774:
https://github.com/nu774/fdkaac_autobuild

Thanks to all of them!

Download
--------

### [Click here to download latest build script](https://github.com/mjb2000/media-autobuild_suite/archive/master.zip)

See the wiki for more information on how to use the script

#### [Click here to download the latest 32-bit binary release with Intel Quicksync support](#)

Included Tools And Libraries
--------

 - ffmpeg (shared or static) with that libraries:
	- decklink
	- fdkaac
	- faac
	- fontconfig
	- freetype
	- frei0r
	- gsm
	- gnutls
	- libass
	- libbluray
	- libcacas
	- libilbc
	- libmfx (for QuickSync support)
	- libmodplug
	- libpng
	- libsoxr
	- libtiff
	- libtwolame
	- libutvideo (only static)
	- libzvbi
	- mp3lame
	- opencore-amr
	- openjpeg
	- ogg
	- opus
	- rtmp
	- schroedinger
	- sdl
	- speex
	- theora
	- vidstab
	- vpx
	- vo-aacenc
	- vo-amrwbenc
	- vorbis
	- wavpack
	- x264
	- x265
	- xavs
	- xvid
	
 - other tools
	- exiv2
	- f265
	- fdkaac
	- faac
	- file
	- flac
	- gnutls
	- kvazaar
	- libsndfile
	- mediainfo cli
	- mp4box
	- mpg123
	- mplayer
	- mkvtoolnix
	- mpv
	- opus-tools
	- rtmp
	- speex
	- sox 
	- vpx
	- x264 (8 and 10 bit, with gpac[mp4 output])
	- x265 (8 and 16 bit)
	- xavs	

Current issues
--------

The latest git version of libvpx does not compile correctly, so I have force a checkout of version 1.3.0 - however since this is not the latest version, each time you run the script, it will try to download the latest git version before reverting to v1.3.0

I have only tested building 32bit static ffmpeg using a 64 architecture

Usage
--------

Please see the [usage page within the Wiki](https://github.com/mjb2000/media-autobuild_suite/wiki/Usage)

References
--------

http://ingar.satgnu.net/devenv/mingw32/base.html
http://kemovitra.blogspot.co.at/2009/08/mingw-to-compile-ffmpeg.html
