## Overview

To simplify the process of using SLAMcore SDK this repository provides a DKMS package that adds support for Intel RealSense D435i and D455 cameras on various ARM platforms. We may also support some of the newer kernels on x86 platforms.

### Requirements

The package has been tested and is compatible with:
* Ubuntu 18.04 (64-bit) on Raspberry Pi 4.
* Nvidia Jetson platforms running L4T versions 32.4.4 through to 32.6.1.
* Ubuntu 20.04 (amd64) running the 5.13 HWE kernel.

## Installation

In order to install the package on a supported platform/OS combination, please download a Debian package from the [Releases section](https://github.com/slamcore/slamcore-dkms/releases). Then install it with `apt` like so:

```
# On arm64 platforms
sudo apt install ./slamcore-dkms_*-bionic_arm64.deb

# On Ubuntu 20.04 for amd64
sudo apt install ./slamcore-dkms_*-focal_amd64.deb
```

And then reboot in order to complete the installation:

```
sudo reboot
```

## License

This repository consists of sources from various [Linux kernel](https://developer.nvidia.com/embedded/l4t/r32_release_v6.1/sources/t186/public_sources.tbz2) [trees](http://ports.ubuntu.com/ubuntu-ports/ubuntu-ports/ubuntu-ports/pool/universe) as well as patches that either come directly from or have been modified based on patches from [librealsense2-dkms](https://github.com/IntelRealsense/librealsense).

The Linux kernel sources are covered by a [variety of licenses](https://github.com/torvalds/linux/tree/master/LICENSES).

The udev rules and the patches that come from Intel Realsense are covered by an [Apache 2 license](https://github.com/IntelRealSense/librealsense/blob/master/LICENSE).

Anything else in this repository that does not come from these sources is covered by an [Apache 2 license](https://github.com/slamcore/slamcore-dkms/blob/master/LICENSE.md).
