# rules_eigen
Bazel rules for building Eigen (https://gitlab.com/libeigen/eigen)

## How to use

In your WORKSPACE.bazel file:

```
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_eigen",
    url = "https://github.com/kgreenek/rules_eigen/archive/eigen-3.4.0-v0.tar.gz",
    sha256 = "668d7503e44daa76e68278373afb04e14e962068dbe461e5ad636bb5c9ea9e5e",
    strip_prefix = "rules_eigen-eigen-3.4.0-v0",
)

load("@rules_eigen//bzl:repositories.bzl", "eigen_repositories")

eigen_repositories()
```
