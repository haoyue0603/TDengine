# Copyright (c) 2017 by TAOS Technologies, Inc.
# todo: library dependency, header file dependency

ROOT=./
TARGET=exe
LFLAGS = '-Wl,-rpath,/usr/local/taos/driver/' -ltaos -lpthread -lm -lrt
CFLAGS = -O0 -g -Wno-deprecated -fPIC -Wno-unused-result -Wconversion \
	-Wno-char-subscripts -D_REENTRANT -Wno-format -D_REENTRANT -DLINUX \
	-Wno-unused-function -D_M_X64 -I/usr/local/taos/include -std=gnu99 -Wno-sign-conversion

all: $(TARGET)

exe:
	gcc $(CFLAGS) ./batchprepare.c  -o $(ROOT)batchprepare  $(LFLAGS)
	gcc $(CFLAGS) ./stopquery.c  -o $(ROOT)stopquery $(LFLAGS)
	gcc $(CFLAGS) ./dbTableRoute.c  -o $(ROOT)dbTableRoute $(LFLAGS)
	gcc $(CFLAGS) ./insertSameTs.c  -o $(ROOT)insertSameTs $(LFLAGS)
	gcc $(CFLAGS) ./passwdTest.c  -o $(ROOT)passwdTest $(LFLAGS)

clean:
	rm $(ROOT)batchprepare
	rm $(ROOT)stopquery
	rm $(ROOT)dbTableRoute
	rm $(ROOT)insertSameTs
	rm $(ROOT)passwdTest
