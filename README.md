# About

This repository contains a basic project which builds into an ARM Cortex-M (STM32) image that can run in QEMU.

Tested in Windows 10 and Ubuntu 16.10.

# Prerequisites

- [GNU ARM Embedded](https://launchpad.net/gcc-arm-embedded) installed and its `bin/` directory in PATH.
- [GNU MCU Eclipse QEMU](https://gnu-mcu-eclipse.github.io/qemu/install/). Note that you don't have to install Eclipse to use this.
- GNU make.

# Usage

```
$ cd Debug
$ make test1.elf
$ qemu-system-gnuarmeclipse -board STM32F429I-Discovery -image test1.elf -nographic
```

Others STM32 boards are supported, see [this link](https://gnu-mcu-eclipse.github.io/qemu/) for details.

The `main` function is defined in `src/main.c`, that's a good place to start hacking. If you need to add more source files or directories to the build, you'll need to modify the makefile in `Debug/makefile` and likely the various `.mk` files under `Debug`.

# License and acknowledgements

Based on [micro-os-plus-iii](https://github.com/micro-os-plus/micro-os-plus-iii) project which is MIT licensed.
This repository is also MIT licensed.