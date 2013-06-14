### Install Android/x86 ISO

* Install Android-x86 into VirtualBox

https://code.google.com/p/android-x86/downloads/list

### Compile Android Linux Kernel for VirtualBox

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


### Enhance Android System

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

### Install busybox

We need the following commands.

* ash
* mknod


### Install Bootchart

### Install Kernel Modules

* Install v4l2 (videodev.ko)
* Install cdata (cdata.ko)

### Deploy Android System

```
# mount -t ext2 /dev/sdb2 /system
# mount -t ext2 /dev/sdb3 /data
# mount -t ext2 /dev/sdb4 /cache
```

* how to well-deploy /data/dalvik-cache and /data/data










