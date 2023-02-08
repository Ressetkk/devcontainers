FROM alpine:edge

RUN apk add --no-cache alpine-sdk build-base apk-tools alpine-conf busybox fakeroot xorriso squashfs-tools sudo \
    && adduser build -D -G abuild \
    && echo "%abuild ALL=(ALL) ALL" > /etc/sudoers.d/abuild \
    && echo "%abuild ALL=(ALL) NOPASSWD:ALL">> /etc/sudoers.d/abuild

USER build