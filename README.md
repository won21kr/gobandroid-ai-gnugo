Build
=====

 - check out gnugo from git://git.savannah.gnu.org/gnugo.git
 - ./configure
 - make
 - make clean ( sounds stupid but we want to get rid of bins but not autogenerated foo )
 - copy all files into the path where you checked out this repo ( do not overwrite any file - skip them )
 - now you can run ndk-build as usual

 
Changelog
=========

 0.1 initial work by Andreas Grothe 
 0.2 NDK 1.5 -> NDK.16 & changes to fit into gobandroid 
 0.7 updates for new NDK (7) and adapt to Gobandroid HD
 1.0 opitmisations for x86

Background
==========

This directory tree contains the NDK build scripts and all files that were modified or added on base of the orignal GNU Go 3.8 sources. To build the android native shared library take the original GNU Go 3.8 sources and replace/add the corresponding files with the files found here. Then generate the pattern files with mkpat.

The changes found here are unfortunally a sad hack. A later version should implement usage of the GTP proocol over sockets (which didn't work at first attempt via JNI). First tries can still be found in interfac/java_bridge.c, but that implementation had issues with buffering of the 'from_gnugo_stream'.

FYI: create patterns in build process https://github.com/ligi/gobandroid-ai-gnugo/issues/1