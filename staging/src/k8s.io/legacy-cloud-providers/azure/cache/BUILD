load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "azure_cache.go",
        "doc.go",
    ],
    importmap = "k8s.io/kubernetes/vendor/k8s.io/legacy-cloud-providers/azure/cache",
    importpath = "k8s.io/legacy-cloud-providers/azure/cache",
    visibility = ["//visibility:public"],
    deps = ["//staging/src/k8s.io/client-go/tools/cache:go_default_library"],
)

go_test(
    name = "go_default_test",
    srcs = ["azure_cache_test.go"],
    embed = [":go_default_library"],
    deps = ["//vendor/github.com/stretchr/testify/assert:go_default_library"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
