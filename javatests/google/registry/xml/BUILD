package(
    default_testonly = 1,
    default_visibility = ["//java/google/registry:registry_project"],
)

licenses(["notice"])  # Apache 2.0

load("//java/com/google/testing/builddefs:GenTestRules.bzl", "GenTestRules")

java_library(
    name = "xml",
    srcs = glob(["*.java"]),
    resources = glob(["testdata/*.xml"]),
    deps = [
        "//java/google/registry/util",
        "//java/google/registry/xml",
        "//javatests/google/registry/testing",
        "@com_google_code_findbugs_jsr305",
        "@com_google_guava",
        "@com_google_truth",
        "@joda_time",
        "@junit",
        "@org_json",
    ],
)

GenTestRules(
    name = "GeneratedTestRules",
    test_files = glob(["*Test.java"]),
    deps = [":xml"],
)
