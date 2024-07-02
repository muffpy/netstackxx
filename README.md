netstackxx is an implementation of a significant portion of the Linux networking stack in C++ including: IP routing, a network interface, and the TCP protocol.

It uses Keith Winstein's ([@keithw](https://github.com/keithw)) minnow [utils](https://github.com/CS144/minnow/tree/main/util) which wrap Linux operating system functions in modern C++ interfaces.

I started this as a side-project in 2021 while learning networking systems and am in the process of migrating the code and docs to GitHub.

> _What, you can’t learn TCP? Then write your own!_
> _— anonymous Zhihu user_

## Environment

netstackxx requires a GNU/Linux operating system and a recent C++ compiler
that supports the C++ 2020 standard.

If you are on macOS or Windows and already have Docker Desktop installed, then you already have Linux installed in the form of a [LinuxKit VM](https://github.com/linuxkit/linuxkit/blob/master/docs/platform-virtualization-framework.md) without the overhead of a full virtual machine like VMware Workstation, VMware Fusion, or VirtualBox.

On your Linux box:
```
sudo apt update && sudo apt install 
git  \
cmake \
gdb \
build-essential \
clang \
clang-tidy \
clang-format \
gcc-doc \
pkg-config \
glibc-doc \
tcpdump \
tshark
```

## Build

To set up the build system: `cmake -S . -B build`

To compile: `cmake --build build`

To run tests: `cmake --build build --target test`

To run speed benchmarks: `cmake --build build --target speed`

To run clang-tidy (which suggests improvements): `cmake --build build --target tidy`

To format code: `cmake --build build --target format`

<!-- ## Components

### Reassembler -->
