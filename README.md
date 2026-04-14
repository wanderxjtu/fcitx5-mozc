# Fcitx5 Mozc

The repo aims to use CMake to build [original project](https://github.com/fcitx/mozc) so that it can be integrated into other platforms more easily.

It is initially created by

```sh
git filter-repo --path src/unix/fcitx5 --force
```

and [src/unix/fcitx5](./src/unix/fcitx5) will be synced from [origin](https://github.com/fcitx/mozc/tree/fcitx/src/unix/fcitx5) regularly.

Build `mozc_data.inc` in case it is missing.
```sh
cd mozc/src
bazelisk build //data_manager/oss:mozc_data.inc --config oss_linux --config release_build
cp bazel-bin/data_manager/oss/mozc_data.inc data_manager/oss/
```
