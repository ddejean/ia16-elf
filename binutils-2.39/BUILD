load("@rules_foreign_cc//foreign_cc:configure.bzl", "configure_make")

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
)

configure_make(
    name = "binutils-2.39",
    configure_options = [
        "--target=ia16-elf",
        "--enable-ld=default",
        "--enable-gold=yes",
        "--enable-targets=ia16-elf",
        "--enable-x86-hpa-segelf=yes",
        "--disable-werror",
        "--disable-libctf",
        "--disable-gdb",
        "--disable-libdecnumber",
        "--disable-readline",
        "--disable-sim",
        "--disable-nls",
    ],
    lib_source = ":srcs",
    out_binaries = [
        "ia16-elf-addr2line",
        "ia16-elf-c++filt",
        "ia16-elf-gprof",
        "ia16-elf-ld.gold",
        "ia16-elf-objdump",
        "ia16-elf-size",
        "ia16-elf-ar",
        "ia16-elf-dwp",
        "ia16-elf-ld",
        "ia16-elf-nm",
        "ia16-elf-ranlib",
        "ia16-elf-strings",
        "ia16-elf-as",
        "ia16-elf-elfedit",
        "ia16-elf-ld.bfd",
        "ia16-elf-objcopy",
        "ia16-elf-readelf",
        "ia16-elf-strip",
    ],
    out_shared_libs = [
        "bfd-plugins/libdep.so",
    ],
    visibility = ["//visibility:public"],
)
