load("@rules_foreign_cc//foreign_cc:configure.bzl", "configure_make")

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
)

configure_make(
    name = "mpc-1.0.3",
    configure_options = [
        "--disable-shared",
        "--with-gmp=$EXT_BUILD_DEPS/gmp-6.1.2",
        "--with-mpfr=$EXT_BUILD_DEPS/mpfr-3.1.5",
    ],
    lib_source = ":srcs",
    out_static_libs = ["libmpc.a"],
    visibility = ["//visibility:public"],
    deps = [
        "@gmp-6.1.2//:gmp-6.1.2",
        "@mpfr-3.1.5//:mpfr-3.1.5",
    ],
)
