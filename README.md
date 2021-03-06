[PokéLibs](https://github.com/pokelibs)

# pgoapi-libs
[![license](https://img.shields.io/github/license/pokelibs/pgoapi-libs.svg?maxAge=2592000?style=flat-square)](https://github.com/pokelibs/pgoapi-libs/blob/master/LICENSE.md)

## Table of Contents

* [What is it?](#what-is-it)
* [Installation](#installation)
* [Documentation](#documentation)
* [Contributing](#contributing)
  * [Core Maintainers](#core-maintainers)
* [Licensing](#licensing)

## What is it?
`pgoapi-libs` is the official source repository for all hashing, encrypt and future libraries that need to be shipped with various API implementations.

## Installation
Simply checkout this repository as a submodule for your project at the desired tagged release.
Please make sure that the SHA256SUMS match up with the sums for each file to assure it hasn't been tampered with.
The latest sums are:

```
b8f62a0fbb301eabbe4cb83bab2c17f35360116b46e196fd53ef5da1d7d1395d  libniahash-freebsd-i386.so
3ffbc2f64ffda74c82cefeff94a7d3aeba72efcc890b847ff2732c308768e6dd  libniahash-freebsd-x86-64.so
e1eff1af978b0fda2b883d38c53290c15de3ca4274b4bd8690d41eab8558843b  libniahash-linux-arm32.so
8fcb0424682df55684410ebb078adc467842f2cf4d2c1b5cc757e461388671df  libniahash-linux-arm64.so
c194a4207eabf0f3e2b418e39747dabeb63aba397a73b27c64eb064e9b344d83  libniahash-linux-i386.so
dd1e9510e58f2793f3f92ec352c8d301e797be473c8aa00d731e5d931f0f76b2  libniahash-linux-x86-64.so
d7290a05cb2b2df36bba3f8205c7940d533b34d43f2e5c8946f32472d82b79a1  libpcrypt-freebsd-i386.so
0bb34ec1bf4e821039f475a724eac74caf160b9a42fe1124a3618e4eb6e25b14  libpcrypt-freebsd-x86-64.so
6d88aad73b495a4d46716a82581cdd4f73dce8b4a5bbf6b24b3c589d36be79e8  libpcrypt-linux-arm32.so
44a00bddbcea475ad283d1498a9d0a30e5a83954fe8d05f60a52cdd6c55b09d2  libpcrypt-linux-arm64.so
87dbd92ba88d399d3b401144c6ca01aa437c14d62f2306bebb374d0717e64479  libpcrypt-linux-i386.so
b3ba09bc70e842aced44733d723ed216464da899878d8601a9c85e4f0f478126  libpcrypt-linux-x86-64.so
549cbc22d4fdee557706ceb70f10c935e995509b2f230272c6c6384c7eb6f925  libniahash-macos-i386.dylib
bfd97a9028a30e711ac5db7967e425f298ca710b5f3c3878c85ffa47df40da76  libniahash-macos-x86-64.dylib
0c9f9838db073422794fabe1d1fbec052bf67e022ba24846d8101ce138b5861b  libpcrypt-macos-i386.dylib
56d030673cb7805387b280578cef3cd64c8ab7a35cdc0c987814730c3b5cc745  libpcrypt-macos-x86-64.dylib
663bec4e8987923c2f82f4aa99c9039c04cf67be6c9eeaec628861ce839c573f  libniahash-windows-i686.dll
c0f9197c67a82b0920293b1a8e2c0a74e1125236c0da7c9d53ab6b7d2b72c70f  libniahash-windows-x86-64.dll
13f82e7ec8539871ef92b8aaa0e40919128ee0df159839d6351fb97e961b6548  libpcrypt-windows-i686.dll
b8faaff74a7a3a8e41784f2884a44f950b50ad8b5209b36f58f90d04570da6e6  libpcrypt-windows-x86-64.dll
```

## Documentation
More detailed instructions on how to compile the given libraries will be updated soon, for now a roughy guideline is given below.

* Checkout https://github.com/laverdet/pcrypt-c (Thanks a lot to @marcel)
* Use `make all`
* Checkout https://gist.github.com/Noctem/018c107d6a6297c24e36a00d4da046c9 (Thanks a lot to @Waryas, @marcel, @HatchingEgg, @Apoc)
* Make the file according to the following flags: (Thanks a lot to @noctem)
```
Linux:
	cc -fPIC -O3 -shared niahash.c -o libniahash-linux-x86-64.so
macOS:
	clang -march=core2 -shared -fPIC -mmacosx-version-min=10.7 -O3 niahash.c -o libniahash-macos-x86-64.dylib
Windows:
	x86_64-w64-mingw32-gcc -O3 -fPIC -shared niahash.c -o libniahash-windows-x86-64.dll
```

## Licensing
[MIT](https://github.com/pokelibs/pgoapi-libs/blob/master/LICENSE)

### Third Party Licenses
    None

## Contributing
Currently, you can contribute to this project by visiting and discussing with us in Discord
