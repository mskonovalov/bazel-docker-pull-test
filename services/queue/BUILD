load("@io_bazel_rules_docker//container:container.bzl", "container_image")

container_image(
    name = "sqs-mock",
    base = "@sqs-mock-base//image",
    files = ["sqs-mock-config"],
    ports = ["4100/tcp", "4200/tcp"],
    directory = "/conf"
)

filegroup(
    name = "sqs-mock-config",
    srcs = glob(["conf/*"]),
)