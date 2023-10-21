load("@rules_foreign_cc//foreign_cc:configure.bzl", "configure_make")

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
)

configure_make(
    name = "gcc-6.3.0",
    configure_options = [
        "--target=ia16-elf",
        "--without-headers",
        "--with-newlib",
        "--enable-languages=c",
        "--disable-libssp",
        "--disable-libquadmath",
        "--disable-libstdcxx",
        "--with-gmp=$EXT_BUILD_DEPS/gmp-6.1.2",
        "--with-mpfr=$EXT_BUILD_DEPS/mpfr-3.1.5",
        "--with-mpc=$EXT_BUILD_DEPS/mpc-1.0.3",
        "--with-isl=$EXT_BUILD_DEPS/isl-0.16.1",
    ],
    # gcc is set as out binary to ensure the rule fails if the build fails.
    # However all the files are packaged using the out_data_dir argument.
    out_binaries = [
        "ia16-elf-gcc",
    ],
    out_data_dirs = [
        "bin",
        "ia16-elf",
        "include",
        "lib",
        "libexec",
        "share",
    ],
    env = {
        "CC": "/usr/bin/gcc",
        "CXX": "/usr/bin/g++",
        "PATH": "$$EXT_BUILD_DEPS/binutils-2.39/bin:$$PATH",
    },
    lib_source = ":srcs",
    visibility = ["//visibility:public"],
    deps = [
        "@gmp-6.1.2//:gmp-6.1.2",
        "@isl-0.16.1//:isl-0.16.1",
        "@mpc-1.0.3//:mpc-1.0.3",
        "@mpfr-3.1.5//:mpfr-3.1.5",
        "@binutils-2.39//:binutils-2.39",
    ],
)
