# Builds a Forth interpreter to embed into a Linux kernel

default: app.o

TOPDIR=../..

#CONFIG += -DBITS32 -DT16 -m32
CONFIG += -DBITS32 -m32

include $(TOPDIR)/src/app/embed-linux/targets.mk

test: test_main.o app.o
	$(CC) $(CFLAGS) test_main.o app.o -o $@

EXTRA_CLEAN += test
