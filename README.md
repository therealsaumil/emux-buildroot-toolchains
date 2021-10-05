# emux-buildroot-toolchains
Precompiled toolchains for ARM and MIPS

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

