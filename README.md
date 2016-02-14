# Bazel-gRPC

A demo of how to use gRPC with Bazel.


* No submodules! Instead, we rely on Bazel's external dependency
  support to fetch git remotes.
* Supports C++ only at the moment.


`bazel build //src:all`
