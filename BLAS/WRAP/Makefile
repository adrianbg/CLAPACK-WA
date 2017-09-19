TOPDIR=../..
include $(TOPDIR)/make.inc

#######################################################################
#  This is the makefile to create a wrapper for the CBLAS.
#######################################################################

all: libcblaswr.bc

libcblaswr.bc: cblaswr.o
	$(LD) $(LDFLAGS) -o $@ $?

libfblaswr.a: fblaswr.o
	$(ARCH) $(ARCHFLAGS) libfblaswr.a fblaswr.o
	$(RANLIB) libfblaswr.a

clean:
	rm -f *.o *.a

.c.o: 
	$(CC) $(CFLAGS) -c $*.c

