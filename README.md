
### Install Android/x86 ISO

1. Install Android-x86 into VirtualBox

https://code.google.com/p/android-x86/downloads/list

2. Download Android Linux Kernel for VirtualBox 

* https://www.kernel.org
* Prefered 3.4 at this moment

3. Get vbox_defconfig

* http://android.googlesource.com

4. Use Android 4.x prebuilt toolchain

5. Replace 

6. Modify video=

* Read Documentation/fb/vesafb.txt

7. Tune e2fs [Optional]

$ sudo tune2fs /dev/sdb1
$ sudo e2fsck -DC0 /deb/sdb1


* Care of toolchain selection


### Enhance Android System

Install pppd
Install stagefright library
Install camera *
[Install VP8]


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

Install v4l2 (videodev.ko)
Install cdata (cdata.ko)

### Deploy Android System

* how to well-deploy /data/dalvik-cache and /data/data










