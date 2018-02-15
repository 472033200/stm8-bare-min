# stm8-bare-min

Tiny peripheral library for STM8S. This library was developed as a supplement to a series of [blog posts](https://lujji.github.io/blog/bare-metal-programming-stm8/) while I was experimenting with STM8 microcontrollers. Tested with SDCC compiler only.

## Code Structure
* `stm8` contains `stm8s.h` header with register definitions and very basic peripheral drivers;
* `examples` contains directories with example code

## Building
Dependencies:
 1. [sdcc](https://sourceforge.net/projects/sdcc/)
 2. [stm8flash](https://github.com/vdudouyt/stm8flash)

Building example project:

```
cd ./examples/<example>
make flash
```
Uncomment `--peep-file $(LIBDIR)/util/extra.def` option in the Makefile to enable additional optimizer rules.

## Bugs
Due to SDCC [Bug #2673](https://sourceforge.net/p/sdcc/bugs/2673/) it is recommended to compile with `--nolospre` flag.
