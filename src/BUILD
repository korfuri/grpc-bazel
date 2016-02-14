load('//:grpc_proto.bzl', 'proto_library')

cc_binary(
    name = 'greeter_client',
    srcs = ['greeter_client.cc'],
    deps = [
        ':helloworld_proto',
        '@grpc//:grpc++',
    ],
    linkopts = ['-ldl'],
)

cc_binary(
    name = 'greeter_server',
    srcs = ['greeter_server.cc'],
    deps = [
        ':helloworld_proto',
        '@grpc//:grpc++',
    ],
    linkopts = ['-ldl'],
)

proto_library(
    name = 'helloworld_proto',
    src = 'helloworld.proto',
    has_service = True,
)
