# abuild-sdk

It's a simple devcontainer that has set-up minimal required settings to work with Alpine's abuild SDK and aports repository.

The image works as user `build` with passwordless `sudo` access.

If you want to use multi-arch devcontainer, configure your Docker instance with [multiarch/qemu-user-static](https://github.com/multiarch/qemu-user-static).

Included packages:

```
alpine-sdk build-base apk-tools alpine-conf busybox fakeroot xorriso squashfs-tools sudo
```

After container creation the abuild RSA keys are created using `sudo abuild-keygen -i -n -a`.

For more information about alpine's SDK, refer to Official Alpine's documentation.

Supported platforms:
* x86_64
* arm64