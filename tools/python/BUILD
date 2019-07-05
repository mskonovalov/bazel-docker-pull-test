load("@bazel_tools//tools/python:toolchain.bzl", "py_runtime_pair")

package(default_visibility = ["//visibility:public"])

py_runtime(
    name = "default_container_py2_runtime",
    interpreter_path = "/nix/store/lbzf4xgg4q1vf9nyh31wwlfsdjijmjr9-python-2.7.16/bin/python2",
    python_version = "PY2",
)

py_runtime(
    name = "default_container_py3_runtime",
    interpreter_path = "/usr/bin/python",
    python_version = "PY3",
)

py_runtime_pair(
    name = "default_container_py_runtime_pair",
    py2_runtime = ":default_container_py2_runtime",
    py3_runtime = ":default_container_py3_runtime",
)

toolchain(
    name = "container_py_toolchain",
    toolchain = ":default_container_py_runtime_pair",
    toolchain_type = "@bazel_tools//tools/python:toolchain_type",
)

# Constraints used to describe docker compatible toolchains.

#constraint_setting(name = "docker")

#constraint_value(
#    name = "run_in_container",
#    constraint_setting = ":docker",
#)
