poplar_recovery_builder.sh is used to create the recovery image for both Debian Linux or Android for Popar.

## Dependencies

1. sfdisk v2.26.2

You probally don't need when running on Ubuntu 16.x. If you are running Ubuntu 14.04, sfdisk needs to be upgraded to a newer version like 2.26.2 in following steps.

```
wget https://www.kernel.org/pub/linux/utils/util-linux/v2.26/util-linux-2.26.2.tar.xz
tar xf util-linux-2.26.2.tar.xz
cd util-linux-2.26.2
./configure
make sfdisk
export PATH=/path/to/util-linux-2.26.2:$PATH
```

2. Install `simg2img` from android-tools-fsutils 
```
apt-get install -y  android-tools-fsutils 
```

3. A new mkimage that supprt arm64 CPU type. 
It come with inside this package for your convenience. You will want to either copy it to your /usr/bin/mkimage, or add it to you `PATH`, export PATH=/path/to/new/mkimage:$PATH

## Instruction for create debian recovery image

https://github.com/96boards-poplar/Documentation/blob/master/debian_build_instructions.md

## Instruction for create Android recovery and flash image

https://github.com/96boards-poplar/Documentation/tree/master/android
