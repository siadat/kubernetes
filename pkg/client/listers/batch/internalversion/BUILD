package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
    "go_test",
    "cgo_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "expansion_generated.go",
        "job.go",
        "job_expansion.go",
        "scheduledjob.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/errors:go_default_library",
        "//pkg/api/unversioned:go_default_library",
        "//pkg/apis/batch:go_default_library",
        "//pkg/client/cache:go_default_library",
        "//pkg/labels:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["job_test.go"],
    library = "go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/unversioned:go_default_library",
        "//pkg/apis/batch:go_default_library",
        "//pkg/client/cache:go_default_library",
        "//pkg/labels:go_default_library",
        "//pkg/util/sets:go_default_library",
    ],
)
