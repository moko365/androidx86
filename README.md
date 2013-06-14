## Install Android/x86 ISO

* Install Android-x86 into VirtualBox

https://code.google.com/p/android-x86/downloads/list

## Compile Android Linux Kernel for VirtualBox

* Download Android Linux Kernel for VirtualBox 

** https://www.kernel.org
** Prefered 3.4 at this moment

*. Get vbox_defconfig

** http://android.googlesource.com

*. Use Android 4.x prebuilt toolchain

*. Replace 

*. Modify video=

* Read Documentation/fb/vesafb.txt

*. Tune e2fs [Optional]

$ sudo tune2fs /dev/sdb1
$ sudo e2fsck -DC0 /deb/sdb1


* Care of toolchain selection


## Enhance Android System

* Install pppd
* Install stagefright library
* Install camera *
* [Install VP8]


```
## in BoardConfig.mk
## Use libstagefright

BUILD_PV_VIDEO_ENCODERS := 1
BUILD_PV_2WAY := 1
BUILD_PV_TEST_APPS := 1
```

## Install busybox

We need the following commands.

* ash
* mknod


## Install Bootchart

## Install Kernel Modules

* Install v4l2 (videodev.ko)
* Install cdata (cdata.ko)

## Deploy Android System

### Partition Layout

```
# mount -t ext2 /dev/sdb2 /system
# mount -t ext2 /dev/sdb3 /data
# mount -t ext2 /dev/sdb4 /cache
```

### fdisk 

```
# fdisk ...
# mkfs.ext2 ...
# tune2fs ...
# e2fsck 
```

### deploy system/

```
android@mokoid-lab:~/mokoid/out/target/product/goldfish $ mkdir mnt
android@mokoid-lab:~/mokoid/out/target/product/goldfish $ sudo mount /dev/sdb2 mnt/
android@mokoid-lab:~/mokoid/out/target/product/goldfish $ cd mnt/
android@mokoid-lab:~/mokoid/out/target/product/goldfish/mnt $ sudo tar zxf /tmp/system.tar.gz 
android@mokoid-lab:~/mokoid/out/target/product/goldfish/mnt $ ls
app/  build.prop  fonts/      lib/         usr/
bin/  etc/        framework/  lost+found/  xbin/
android@mokoid-lab:~/mokoid/out/target/product/goldfish/mnt $ cd ..
android@mokoid-lab:~/mokoid/out/target/product/goldfish $ sudo umount mnt
```

### deploy ramdisk.img and bzImage

### Modify init.rc

### Install Grub

* Use grub-install
* how to well-deploy /data/dalvik-cache and /data/data

### Installation CD













