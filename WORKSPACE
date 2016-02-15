# grpc is required for this project
git_repository(
    name = 'grpc',
    remote = 'https://github.com/grpc/grpc.git',
    commit = 'b14f6e6f61ea4a67f05a6c7e28ca1e6e5f01f445',
)

# protobuf and a couple bindings are required by grpc
git_repository(
    name = 'protobuf',
    remote = 'https://github.com/google/protobuf.git',
    commit = 'e35e24800fb8d694bdeea5fd63dc7d1b14d68723',
)

bind(
    name = 'protobuf_compiler',
    actual = '@protobuf//:protoc_lib',
)

bind(
    name = 'protobuf_clib',
    actual = '@protobuf//:protobuf',
)

# boringssl or openssl is required by grpc
new_git_repository(
    name = 'boringssl',
    remote = 'https://boringssl.googlesource.com/boringssl',
    commit = '82aa28fa81222a4a614ccf43fbc5b6e9bf02b588',
    build_file = 'BUILD.boringssl',
)

# Go is required to generate some parts of BoringSSL
load("@bazel_tools//tools/build_rules/go:def.bzl", "go_repositories")
go_repositories()

bind(
    name = 'libssl',
    actual = '@boringssl//:ssl',
)

# zlib is required by grpc
new_git_repository(
    name = 'zlib_repo',
    remote = 'https://github.com/madler/zlib.git',
    commit = '50893291621658f355bc5b4d450a8d06a563053d',
    build_file = 'BUILD.zlib',
)

bind(
    name = 'zlib',
    actual = '@zlib_repo//:zlib',
)
