obj-m := cdata.o

KDIR := /usr/src/linux-headers-2.6.24-26-generic
PWD := $(shell pwd)

default:
	$(MAKE) -C $(KDIR) SUBDIRS=$(PWD) modules

clean:
	rm -rf *.o *.ko .*cmd modules.* Module.* .tmp_versions *.mod.c
