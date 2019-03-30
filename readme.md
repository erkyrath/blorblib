Blorblib version 1.0.2

- Designed by Andrew Plotkin <erkyrath@eblong.com>
- http://www.eblong.com/zarf/blorb/index.html

Blorblib is a C library for manipulating [Blorb][] files.

*Caveat:* This library has not been updated since early 2000 (Blorb spec
1.1). It is obsolete and not maintained. I've posted it only for the benefit
of legacy projects.

You will probably want to change the lines

    typedef unsigned long uint32;
    typedef unsigned short uint16;

...in blorb.h to

    typedef uint32_t uint32;
    typedef uint16_t uint16;

A more current C implementation is included with [CheapGlk][].
For a current Blorb manipulation tool, see [blorbtool.py][].

[Blorb]: http://www.eblong.com/zarf/blorb/index.html
[CheapGlk]: https://github.com/erkyrath/cheapglk
[blorbtool.py]: https://github.com/erkyrath/glk-dev/blob/master/blorbtool.py

---

This package contains:

- readme.md: This file.
- blorblib.txt: Documentation for blorblib.
- blorb.h: The header for blorblib, suitable for including in an interpreter.
- blorblib.c: The source code for blorblib.
- blorblow.h: Low-level definitions for blorblib.
- blorbscan.c: A program to read and analyze Blorb files.

To compile blorbscan, do

    gcc -o blorbscan blorbscan.c blorblib.c

or the equivalent. Run the program with no arguments to see a list of
options, or give it the name of a Blorb file.

To add blorblib to a Z-machine interpreter, see blorblib.txt.

The source code in this package is copyright 1998-2000 by Andrew
Plotkin. It is distributed under the MIT license; see the "LICENSE"
file.
