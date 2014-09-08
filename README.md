This utility is a fork of the Hairless-MidiSerial project by projectgus (http://projectgus.github.io/hairless-midiserial/)

This utility adds the ability to control Serial devices by using physical MIDI controls. This is a project primarily aimed at Software Defined Radios in the Amateur Radio world but can be used to control any serial device using its specific Serial commands.

Those serial commands can be mapped to individual channel / notes of the MIDI devices.

This utility is currently only available for Windows. Support for Mac OS and Linux might be added in the future if I can figure out how to cross-compile for those platforms.


Old Instructions left as-is -
===========================

# Building Hairless Bridge from source

(Note again, prebuilt versions *are available for download* at the above URL.)

Hairless Midiserial Bridge release 0.4 was built with Qt 4.7.3. It's also been built and run under Qt 4.7.4. Newer Qt versions 4.8 or 5.0 will probably require code changes in order to compile and/or run.

The Qt package should contain all dependencies, the graphical IDE "Qt Creator" or the program "qmake" can be used to compile the project hairless-midiserial.pro.

The libraries (RtMidi & qextserialport) used by Hairless Bridge are included directly in this source tree to be compiled in.

On Windows I recommend building with the [MingGW compiler](http://www.mingw.org/), Visual Studio has not been tested. Neither the MinGW site nor Qt's new owners Digia still distribute older MinGW builds, and MinGW 4.7 is too new for precompiled Qt 4.7.x, so it can be a bit hard to find a prebuilt combination that work. Recently I downloaded mingw-static-4.4.5-all.7z from [this Google Code project](https://code.google.com/p/qp-gcc/downloads/list), and can confirm that works.

(For the Windows release builds I actually [cross-build under Linux using wine, as described here](http://projectgus.com/2011/09/developing-qt-apps-for-windows-using-linux-wine/).)

# Release builds

The official releases are static linked, so they've actually been built against Qt versions that were compiled from source, configured with "-static" for static linking.
