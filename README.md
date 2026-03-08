# openwrt-patches
Patches for OpenWrt.

## Usage

1. Install quilt

    ```shell
    sudo apt install quilt
    ```

2. [Prepare quilt configuration](https://openwrt.org/docs/guide-developer/toolchain/use-patches-with-buildsystem#prepare_quilt_configuration)

    ```shell
    cp .quiltrc ~/.quiltrc
    ```

3. Apply patches

    ```shell
    cd openwrt
    cp -r /path/to/patches ./
    quilt push -a
    ```

### Refreshing patches

```shell
quilt pop -a
quilt push # patch1
quilt refresh
quilt push # patch2
quilt refresh
# ...

# while quilt push; do
#   quilt refresh
# done
```
