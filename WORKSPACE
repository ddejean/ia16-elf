# Copyrigh (C) 2023 - Damien Dejean <dam.dejean@gmail.com>

workspace(name = "ia16-elf")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_foreign_cc",
    sha256 = "2a4d07cd64b0719b39a7c12218a3e507672b82a97b98c6a89d38565894cf7c51",
    strip_prefix = "rules_foreign_cc-0.9.0",
    url = "https://github.com/bazelbuild/rules_foreign_cc/archive/0.9.0.tar.gz",
)

load("@rules_foreign_cc//foreign_cc:repositories.bzl", "rules_foreign_cc_dependencies")

rules_foreign_cc_dependencies()

http_archive(
    name = "gmp-6.1.2",
    build_file = "@//gmp-6.1.2:BUILD",
    sha256 = "5275bb04f4863a13516b2f39392ac5e272f5e1bb8057b18aec1c9b79d73d8fb2",
    strip_prefix = "gmp-6.1.2",
    url = "https://gmplib.org/download/gmp/gmp-6.1.2.tar.bz2",
)

http_archive(
    name = "mpfr-3.1.5",
    build_file = "@//mpfr-3.1.5:BUILD",
    sha256 = "ca498c1c7a74dd37a576f353312d1e68d490978de4395fa28f1cbd46a364e658",
    strip_prefix = "mpfr-3.1.5",
    url = "https://www.mpfr.org/mpfr-3.1.5/mpfr-3.1.5.tar.bz2",
)

http_archive(
    name = "mpc-1.0.3",
    build_file = "@//mpc-1.0.3:BUILD",
    sha256 = "617decc6ea09889fb08ede330917a00b16809b8db88c29c31bfbb49cbf88ecc3",
    strip_prefix = "mpc-1.0.3",
    url = "https://ftp.gnu.org/gnu/mpc/mpc-1.0.3.tar.gz",
)

http_archive(
    name = "isl-0.16.1",
    build_file = "@//isl-0.16.1:BUILD",
    sha256 = "412538bb65c799ac98e17e8cfcdacbb257a57362acfaaff254b0fcae970126d2",
    strip_prefix = "isl-0.16.1",
    url = "https://gcc.gnu.org/pub/gcc/infrastructure/isl-0.16.1.tar.bz2",
)

http_archive(
    name = "binutils-2.39",
    build_file = "@//binutils-2.39:BUILD",
    sha256 = "3148c38798e906fc7175f00ac3c6f5b3a198eea9e0bd98e18cfaa6d83fb65c2e",
    strip_prefix = "binutils-ia16-binutils-ia16-tkchia",
    url = "https://gitlab.com/tkchia/binutils-ia16/-/archive/binutils-ia16-tkchia/binutils-ia16-binutils-ia16-tkchia.tar.gz",
)

http_archive(
    name = "gcc-6.3.0",
    build_file = "@//gcc-6.3.0:BUILD",
    sha256 = "ddad38254c62a7903b9669930b63e4e34babf3015b0487c59ace52462bd8b4a5",
    strip_prefix = "gcc-ia16-gcc-6_3_0-ia16-tkchia",
    url = "https://gitlab.com/tkchia/gcc-ia16/-/archive/gcc-6_3_0-ia16-tkchia/gcc-ia16-gcc-6_3_0-ia16-tkchia.tar.gz",
)
