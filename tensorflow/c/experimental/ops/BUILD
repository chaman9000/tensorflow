# Experimental ops. These will eventually be replaced by machine-generated versions.
package(
    licenses = ["notice"],  # Apache 2.0
)

cc_library(
    name = "array_ops",
    srcs = [
        "array_ops.cc",
    ],
    hdrs = [
        "array_ops.h",
    ],
    visibility = [
        "//tensorflow:internal",
    ],
    deps = [
        "//tensorflow/c/eager:abstract_context",
        "//tensorflow/c/eager:abstract_operation",
        "//tensorflow/c/eager:abstract_tensor_handle",
        "//tensorflow/c/eager:c_api_unified_internal",
        "//tensorflow/core/lib/llvm_rtti",
        "//tensorflow/core/platform:errors",
    ],
)

cc_library(
    name = "math_ops",
    srcs = [
        "math_ops.cc",
    ],
    hdrs = [
        "math_ops.h",
    ],
    visibility = [
        "//tensorflow:internal",
    ],
    deps = [
        ":array_ops",
        "//tensorflow/c/eager:abstract_context",
        "//tensorflow/c/eager:abstract_tensor_handle",
        "//tensorflow/c/eager:c_api_unified_internal",
        "//tensorflow/core:framework",
        "//tensorflow/core/lib/llvm_rtti",
        "//tensorflow/core/platform:errors",
    ],
)

cc_library(
    name = "nn_ops",
    srcs = [
        "nn_ops.cc",
    ],
    hdrs = [
        "nn_ops.h",
    ],
    visibility = [
        "//tensorflow:internal",
    ],
    deps = [
        "//tensorflow/c/eager:abstract_operation",
        "//tensorflow/c/eager:abstract_tensor_handle",
        "//tensorflow/c/eager:c_api_unified_internal",
        "//tensorflow/core/lib/llvm_rtti",
        "//tensorflow/core/platform:errors",
    ],
)

cc_library(
    name = "ops",
    visibility = [
        "//tensorflow:internal",
    ],
    deps = [
        ":array_ops",
        ":math_ops",
        ":nn_ops",
    ],
)

filegroup(
    name = "pywrap_required_hdrs",
    srcs = [
        "array_ops.h",
        "math_ops.h",
        "nn_ops.h",
    ],
    visibility = [
        "//tensorflow/core:__pkg__",
        "//tensorflow/python:__pkg__",
    ],
)
