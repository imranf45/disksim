

include .paths

CC = cc -m32

CFLAGS = -g $(DISKSIM_CFLAGS) $(DISKMODEL_CFLAGS) $(LIBPARAM_CFLAGS) $(LIBDDBG_CFLAGS) -Wall -Wno-unused

LDFLAGS = $(DISKSIM_LDFLAGS)  $(MEMSMODEL_LDFLAGS) $(SSDMODEL_LDFLAGS) -L.. -ldiskmodel  $(LIBPARAM_LDFLAGS) $(LIBDDBG_LDFLAGS) -lm

TARGETS = g4_skews
all: $(TARGETS)

%: %.o
	$(CC) $(CFLAGS) -o $@ $< $(LDFLAGS)

%: %.c


clean:
	rm -f *.o $(TARGETS)

distclean: clean
	rm -f *~
