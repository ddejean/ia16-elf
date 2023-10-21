load("@rules_foreign_cc//foreign_cc:configure.bzl", "configure_make")

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
)

configure_make(
    name = "gmp-6.1.2",
    configure_options = ["--disable-shared"],
    lib_source = ":srcs",
    out_static_libs = ["libgmp.a"],
    visibility = ["//visibility:public"],
)