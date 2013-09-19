Report for lab1
====================

Installing gcc in Mac OS X
---------------------

Using brew to install gmp, mpfr, libmpc before configuring gcc:
```shell
brew install gmp
brew install mpfr
brew install libmpc
```

build outside of the source tree of gcc:
```shell
mkdir build 
cd build
../configure --target=i386-jos-elf --disable-nls --without-headers --with-newlib --disable-threads --disable-shared --disable-libmudflap --disable-libssp
```

Installing qemu 
---

```shell
./configure --target-list="i386-softmmu" --disable-kvm --disable-sdl
make
make install
```