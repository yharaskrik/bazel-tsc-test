package(default_visibility = ["//visibility:public"])

load("@npm//@bazel/typescript:index.bzl", "ts_config", "ts_library")

ts_library(
  name = "app",
  srcs = ["index.ts"],
  deps = ["//command"],
)

load("@npm//@bazel/rollup:index.bzl", "rollup_bundle")

rollup_bundle(
    name = "bundle",
    entry_point = "index.ts",
    deps = [
        ":app",
    ],
)
