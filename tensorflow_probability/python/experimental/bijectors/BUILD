# Copyright 2020 The TensorFlow Probability Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
# ============================================================================
# tfp.experimental distributions library.

load(
    "//tensorflow_probability/python:build_defs.bzl",
    "multi_substrate_py_library",
    "multi_substrate_py_test",
)

package(
    default_visibility = [
        "//tensorflow_probability:__subpackages__",
    ],
)

licenses(["notice"])

exports_files(["LICENSE"])

multi_substrate_py_library(
    name = "bijectors",
    srcs = ["__init__.py"],
    srcs_version = "PY3",
    deps = [
        ":scalar_function_with_inferred_inverse",
    ],
)

multi_substrate_py_library(
    name = "scalar_function_with_inferred_inverse",
    srcs = ["scalar_function_with_inferred_inverse.py"],
    srcs_version = "PY3",
    deps = [
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability/python/bijectors:bijector",
        "//tensorflow_probability/python/internal:custom_gradient",
        "//tensorflow_probability/python/internal:prefer_static",
        "//tensorflow_probability/python/internal:tensor_util",
        "//tensorflow_probability/python/math",
    ],
)

multi_substrate_py_test(
    name = "scalar_function_with_inferred_inverse_test",
    size = "medium",
    srcs = ["scalar_function_with_inferred_inverse_test.py"],
    jax_size = "medium",
    srcs_version = "PY3",
    deps = [
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability",
        "//tensorflow_probability/python/internal:test_util",
    ],
)
