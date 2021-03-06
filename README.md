[![License](http://img.shields.io/:license-apache-blue.svg?style=flat-square)](http://www.apache.org/licenses/LICENSE-2.0.html)


## Introduction

This project aims to provide cloud-init enabled debian lxd images.

The image is based on the default Debian Stretch/Buster amd64 image that you can find [here](https://images.linuxcontainers.org/).


## Modifications

we have added the following packages to the images:
```
cloud-init cloud-initramfs-dyn-netconf ssh sudo python-minimal
``` 


## Usage

For Debian Stretch use
```bash
lxc image import https://lxd.valet.sh/debian-stretch-cloud-init/ --alias debian-stretch-cloud-init
```

For Debian Buster use
```bash
lxc image import https://lxd.valet.sh/debian-buster-cloud-init/ --alias debian-buster-cloud-init
```

If you are using LXD 3.0.1 this command will not work (see [Issue#4919](https://github.com/lxc/lxd/issues/4919)). If you can not upgrade to more recent version of lxd you have to download and import the image manually.


## License

[Apache v2](./LICENSE.md)