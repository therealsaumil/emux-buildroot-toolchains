# emux-buildroot-toolchains
by Saumil Shah

Precompiled toolchains for ARM and MIPS with GCC 4.3.x and uClibc

*NEW*
Precompiled toolchains for AARCH64 with GCC 8.x and uClibc


## How to build from source

First, get the `buildroot-2012.08` source tree.
```
git clone --depth 1 --branch 2012.08 https://github.com/buildroot/buildroot.git
```
Copy the `{ARCH}-defconfig` file in it. For example:
```
cp mips-defconfig buildroot/
cd buildroot/
make defconfig BR2_DEFCONFIG=mips-defconfig
make
```
The compilation will take a long time. Grab the toolchain tree from `output/host/usr/`.

## How to build the aarch64 toolchain from source

First, get the `buildroot-2017.02` source tree.
```
git clone --depth 1 --branch 2017.02 https://github.com/buildroot/buildroot.git
```
Copy the `aarch64-defconfig` file in it. For example:
```
cp aarch64-defconfig buildroot/
cd buildroot/
make defconfig BR2_DEFCONFIG=aarch64-defconfig
make
```
The compilation will take a long time. Grab the toolchain tree from `output/host/usr/`.

