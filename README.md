BDInfo - Display Blu-ray disc media info
========================================

This program is written in C# and targets .NET 2.0.  It is able to parse and display the video metadata on Blu-ray discs.

It seems that the original developer's website has gone offline:

http://cinemasquid.com/

This repository hosts the latest source code from there.  Additional features or bug fixes may (or may not) be authored here.

The application icon is part of the "Build Icons by Umar123" and is licensed as CC Attribution-Share Alike 4.0:

http://www.iconarchive.com/show/build-icons-by-umar123.html


Building using Mono on Linux
----------------------------

Mono version 3.2.8 (which is shipped at least as of Ubuntu 15.04) is not new enough.  You'll need to get an updated version:

http://www.mono-project.com/docs/getting-started/install/linux

If you're building on Ubuntu 16.04, the packaged version of Mono (4.2.1) is new enough to build this.  You'll need the
following packages installed build and run:

* mono-runtime
* libmono-system-windows-forms4.0-cil
* mono-xbuild (only at build time)

Then you can build the project as follows:

> xbuild /p:Configuration=Release BDInfo.sln

Cleaning up after a build:

> xbuild /p:Configuration=Release /t:Clean BDInfo.sln
