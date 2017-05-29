
AUTOMAKE_OPTIONS = foreign
GIT_VERSION := $(shell git describe --abbrev=8 --dirty --always --tags)

AM_CFLAGS = -DVERSION=\"$(VERSION)\" -DPROG="\"$(PACKAGE)\"" -D_FILE_OFFSET_BITS=64 \
	-D_BSD_SOURCE \
	-I$(top_srcdir)/src \
	-DGIT_VERSION=\"$(GIT_VERSION)\" -Wall -O3 --std=c99

LDADD = ../src/libballistics.la -lballistics -lm

example_SOURCES = example.c

bin_PROGRAMS  = example

