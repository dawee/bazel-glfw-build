load("@rules_foreign_cc//foreign_cc:defs.bzl", "cmake")

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
    visibility = ["//visibility:public"],
)

cmake(
    name = "assimp",
    generate_args = ["-DBUILD_SHARED_LIBS=OFF", "-DASSIMP_WARNINGS_AS_ERRORS=OFF"],
    lib_source = ":srcs",
    out_static_libs = ["assimp-vc143-mt.lib", "zlibstatic.lib"],
    visibility = ["//visibility:public"],
)
