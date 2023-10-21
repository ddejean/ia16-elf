load("@rules_foreign_cc//foreign_cc:configure.bzl", "configure_make")

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
)

configure_make(
    name = "isl-0.16.1",
    configure_options = [
        "--disable-shared",
        "--with-gmp-prefix=$EXT_BUILD_DEPS/gmp-6.1.2",
    ],
    lib_source = ":srcs",
    out_static_libs = ["libisl.a"],
    visibility = ["//visibility:public"],
    deps = [
        "@gmp-6.1.2//:gmp-6.1.2",
    ],
)
