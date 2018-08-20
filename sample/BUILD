load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")

objc_library(
    name = "AppClasses",
    srcs = [
         "App/AppDelegate.m",
         "App/ViewController.m",
         "App/main.m",
    ],
    hdrs = glob(["App/*.h"]),
    xibs = ["App/ViewController.xib"],
)

ios_application(
    name = "sample",
    bundle_id = "Bazel.App",
    families = [
        "iphone",
        "ipad",
    ],
    minimum_os_version = "9.0",
    infoplists = [":App/Info.plist"],
    visibility = ["//visibility:public"],
    deps = [":AppClasses"],
)