# ia16-elf toolchain

This repository provides an IA16 toolchain, based on [gcc-ia](https://gitlab.com/tkchia/gcc-ia16) project by TK Chia. The rules provided here help to build the toolchain using Bazel and provides a workspace to allow projects to depend on it.

To build the toolchain, run:

```
bazel build @gcc-6.3.0//:gcc-6.3.0
```

Related links:
* gcc-ia16: https://gitlab.com/tkchia/gcc-ia16
* build-ia16: https://gitlab.com/tkchia/build-ia16
