filegroup(
    name = "srcs",
    srcs = glob(["**"]) + ["//src/tools/launcher/util:srcs"],
    visibility = ["//src:__pkg__"],
)

cc_binary(
    name = "launcher",
    srcs = ["launcher_main.cc"],
    visibility = [
        "//src:__pkg__",
        "//tools/launcher:__pkg__",
    ],
    deps = [
        ":bash_launcher",
        ":java_launcher",
        ":launcher_base",
        ":python_launcher",
        "//src/tools/launcher/util",
        "//src/tools/launcher/util:data_parser",
    ],
)

cc_library(
    name = "launcher_base",
    srcs = ["launcher.cc"],
    hdrs = ["launcher.h"],
    deps = [
        "//src/tools/launcher/util",
        "//src/tools/launcher/util:data_parser",
    ],
)

cc_library(
    name = "java_launcher",
    srcs = ["java_launcher.cc"],
    hdrs = ["java_launcher.h"],
    deps = [":launcher_base"],
)

cc_library(
    name = "python_launcher",
    srcs = ["python_launcher.cc"],
    hdrs = ["python_launcher.h"],
    deps = [":launcher_base"],
)

cc_library(
    name = "bash_launcher",
    srcs = ["bash_launcher.cc"],
    hdrs = ["bash_launcher.h"],
    deps = [":launcher_base"],
)
