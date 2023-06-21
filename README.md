# rules_eigen
Bazel rules for building Eigen (https://gitlab.com/libeigen/eigen)

## How to use

In your WORKSPACE file:

```
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_eigen",
    url = "https://github.com/kgreenek/rules_eigen/archive/eigen-3.4.0-v0.tar.gz",
    sha256 = "[TODO SHA for release]",  # TODO(kgk): Update this as a follow-up commit after merging and tagging.
    strip_prefix = "eigen-3.4.0-v0",
)

load("@rules_eigen//bzl:repositories.bzl", "eigen_repositories")

eigen_repositories()
```
