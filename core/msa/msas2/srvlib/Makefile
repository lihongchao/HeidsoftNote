prefix = /app/msa/
bindir = /app/msa/bin
libdir = /app/msa/msas2/lib
srcdir = /app/msa/msas2
sqldir = /app/sqldb/include
publicdir = /app/msa/publiclib

CFLAGS:= -O2 -nostartfiles   -Wall -Wunused  -Iinclude -I${publicdir}/include -I${srcdir}/include \
-I${sqldir} -I/usr/include/libxml2/ -DNO_SHARED_LIBS=1

all: srv-test.o srv-module.o
	ar rv ${libdir}/srvlib.a  *.o

clean: 
	rm -f  ${libdir}/srvlib.a *.o
	
srv-test.o: srv-test.c
	gcc -c  srv-test.c  $(CFLAGS)	
		
srv-module.o: srv-module.c
	gcc -c  srv-module.c  $(CFLAGS)
