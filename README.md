# [magika](https://securityresearch.google/magika/) in a snap #

-------------------------------------------------------------------------------

[![magika](https://snapcraft.io/magika/badge.svg)](https://snapcraft.io/magika)

## Installation ##

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/magika)

``` shell
sudo snap install magika
```

To analyse files stored on an external USB drive or similar, ensure you manually connect the removable-media interface after installing the snap:

    snap connect magika:removable-media

([Don't have snapd installed?](https://snapcraft.io/docs/core/install))

## Smoke tests

Spread runs the smoke test on Ubuntu 24.04 and 26.04 cloud images using
Image Garden. Install the `image-garden` snap and run on a host with
access to `/dev/kvm`.

Run `snapcraft pack` in the repository root, then run
`image-garden.spread` to test all four `latest` store channels and the newest
local `magika_*.snap` by modification time. Use
`image-garden.spread tests/smoke:local` to test only the local build, or
`image-garden.spread tests/smoke:latest_stable` to test only the stable channel.
