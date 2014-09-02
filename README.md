PAC-man - The AIO ROM for armv6 devices
=====================

Getting Started
---------------

The first thing to do is prepare your machine to build, [use this guide for that!](https://github.com/PAC-man/android_vendor_pac/blob/pac-4.4/PrepareForBuild.md) if your machine is already configured to build, skip this step

After preparing your machine, continue with the following instructions:

To initialize your local repository using the PAC-man trees, use a command like this:

    repo init -u git://github.com/Fagyi/pacman.git -b <branch>

To initialize for KitKat

    repo init -u git://github.com/Fagyi/pacman.git -b pac-4.4

Then to sync up:

    repo sync -j#

Where # is the specific number of Jobs, 4 is default, change in accordance to internet performance/bandwidth/speed. Default is 4.

Then to build:

    ./build-pac.sh <device_code_name>

Example for ZTE Skate:

    ./build-pac.sh skate

For a list of supported commands run the script on it's own:

    ./build-pac.sh

To build with flags, this is the layout needed:
    ./build-pac.sh <Optional_flags> <device codename>

For an o3 optimization and Dex optimisations -if you don't understand, best to leave it- for the ZTE Skate run:

    ./build-pac.sh -o3 -d skate

You can also add a -j# before device_code_name for a selected number of jobs, usually No. of cores + 1 or 2


Device isn't supported? Not a problem, see [Adding Support] (https://github.com/PAC-man/android_vendor_pac/blob/pac-4.4/README.md) for how to add device support!

For information on how to build a general ROM from source, check [Here](http://forum.xda-developers.com/showthread.php?t=2649812)
