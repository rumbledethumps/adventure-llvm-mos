Colossal Cave Adventure
=======================

This is the real, full-blown Colossal Cave Adventure game, written by
Will Crowther and Don Woods at Stanford AI Lab in the early '70s.  It is
the first interactive fiction game where the computer simulates and
describes a situation, and the user types in what to do next, in simple
English.

```
You are standing at the end of a road before a small brick building.
Around you is a forest.  A small stream flows out of the building and
down a gully.

> █
```


This DOES NOT WORK
------------------

This repo is part of an effort to make it work on llvm-mos. If you want a working game, [go here](https://github.com/picocomputer/adventure) for the cc65 version.


```
[main] Building folder: /home/rumble/adventure-llvm-mos/build
[build] Starting build
[proc] Executing command: /usr/bin/cmake --build /home/rumble/adventure-llvm-mos/build --config Debug --target all -j 18 --
[build] [ 12%] Building C object CMakeFiles/advent.dir/src/err.c.obj
[build] [ 25%] Linking C executable advent
[build] ld.lld: error: section '.text' will not fit in region 'ram': overflowed by 23179 bytes
[build] ld.lld: error: section '.rodata' will not fit in region 'ram': overflowed by 37295 bytes
[build] ld.lld: error: section '.data' will not fit in region 'ram': overflowed by 38540 bytes
[build] ld.lld: error: section '.data' will not fit in region 'ram': overflowed by 38540 bytes
[build] ld.lld: error: section '.bss' will not fit in region 'ram': overflowed by 40107 bytes
[build] ld.lld: error: section '.noinit' will not fit in region 'ram': overflowed by 40109 bytes
[build] mos-rp6502-clang: error: ld.lld command failed with exit code 1 (use -v to see invocation)
[build] gmake[2]: *** [CMakeFiles/advent.dir/build.make:194: advent] Error 1
[build] gmake[1]: *** [CMakeFiles/Makefile2:100: CMakeFiles/advent.dir/all] Error 2
[build] gmake: *** [Makefile:91: all] Error 2
[proc] The command: /usr/bin/cmake --build /home/rumble/adventure-llvm-mos/build --config Debug --target all -j 18 -- exited with code: 2
[driver] Build completed: 00:00:00.883
[build] Build finished with exit code 2
```
