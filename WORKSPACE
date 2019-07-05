load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_docker",
    sha256 = "87fc6a2b128147a0a3039a2fd0b53cc1f2ed5adb8716f50756544a572999ae9a",
    strip_prefix = "rules_docker-0.8.1",
    urls = ["https://github.com/bazelbuild/rules_docker/archive/v0.8.1.tar.gz"],
)

register_toolchains("//tools/python:container_py_toolchain")

load("@io_bazel_rules_docker//repositories:repositories.bzl", container_repositories = "repositories")

container_repositories()

load("@io_bazel_rules_docker//container:container.bzl", "container_pull")

container_pull(
    name = "sqs-mock-base",
    registry = "index.docker.io",
    repository = "pafortin/goaws",
    digest = "sha256:8b7a55b056b7ecb3b2fd19182f18a019662174faa80031840db58ec3312bfdb5"
)
