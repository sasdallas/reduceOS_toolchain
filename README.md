# reduceOS_toolchain
The toolchain for the reduced operating system (GCC-Binutils).

## What is this?
The reduceOS toolchain is a modified version of GCC and binutils to allow compilation of apps for reduceOS.\
While reduceOS has its own C library (newlib), we still need to modify copies of GCC/binutils to automatically use that library.\
This buildscript and these patches will ensure that this can be done.

## How do I build and use it?
You can use the `build_tools.sh` script to easily download and build the toolchain.\
After, you can use `i686-reduceOS-gcc` to compiler applications for reduceOS.

## Can I port programs using this?
Yes! If an application uses make and relies only on cli, you can (probably) just call `make CC=i686-reduceOS-gcc CXX=i686-reduceOS-g++ LD=i686-reduceOS-ld...` to force the Makefile to use reduceOS tools.

A warning that not all applications are compatible with reduceOS due to differences. The /dev/ directory has been replaced with /device/ and device names are different.

## Is there a Docker image?
Not currently. Cry about it.
