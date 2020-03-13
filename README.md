# 4k-intro-sprites-are-us
This is a litte (only 4KB) intro I wrote in 2004. It was an attempt to showcase that it is quite possible to generate a tiny executable that actually does something (3d graphics and audio) using a high level language such as C/CPP.

[![Preview](https://img.youtube.com/vi/bIwQHldMUBk/0.jpg)](https://youtu.be/bIwQHldMUBk)

It consists of 100.000 circular sprites drawn using DirectX 9 that are alpha blended together. Of course its eats up lots of bandwidth :-D

Some friends and I were wondering what we can do if we have a 4096 byte executable size limit. This was my contribution to the contest.

SpritesAreUs features 100.000 sprites each colored using a pseudo random number drawn using DirectX-9 and includes a public domain MIDI soundtrack (details in the file mucke.h). The sprites are animated in differend animation patterns and morph into an starfield at the end.

To reach the goal of 4096 the PE Executable is packed into an old faschioned .com executable because the header is much smaller (the smallest PE header has 512 bytes w/o payload).

The pseudo random numbers are generated using the realtime stamp counter of the CPU.

Bear in mind that a small size of the executable was the prime goal of this project. To achieve this all error checks and memory freeing operations have been diliberatly removed.

The youtube video was heavly compressed by youtube and runs only at 30 FPS. On decent hardware it easly runs at 60 FPS.

You also need a 32 bit Windows system such as Windows XP (the target OS) because .com files are no longer supported in 64 Bit operating systems. 

It appears to run fine in VMs with 3D acceleration enabled.