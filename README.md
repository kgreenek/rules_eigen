# rules_eigen
Bazel rules for building Eigen (https://gitlab.com/libeigen/eigen)

## How to use

In your WORKSPACE.bazel file:

```
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_eigen",
    url = "https://github.com/kgreenek/rules_eigen/archive/eigen-3.4.0-v0.tar.gz",
    sha256 = "8de840654f85a8a474e0e80ba1da6fdedf82bb7720fad8061ac79a2def4f52c0",
    strip_prefix = "rules_eigen-eigen-3.4.0-v0",
)

load("@rules_eigen//bzl:repositories.bzl", "eigen_repositories")

eigen_repositories()
```
