Remember The Milk Simple
========================

**This project is experimental. Use at your own risk.**

A simplified version the Remember The Milk widget from kdeplasma-addons.
You need to have the Remember The Milk dataengine installed, usually by 
installing kdeplasma-addons.

![](http://hanswchen.files.wordpress.com/2011/09/rememberthemilk-simple.png)

Installation
------------

If possible, it is recommended that you install this widget through your package manager.
The typical procedure to compile it from source is as follows:

    mkdir build
    cd build
    cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` ..
    make
    make install

The last command usually requires root permissions so you probably need to use `su`/`sudo`
or similar commands.
