CC = g++
RM = rm
CP = cp

CFLAGS = -O3 `root-config --cflags` -Wall -c
LIBS =  `root-config --libs` -Wall

channel_to_ns: channel_to_ns.o
	$(CC) -o $@ $(LIBS) $<

.cpp.o:
	$(CC) $(CFLAGS) $<

clean:
	$(RM) *.o channel_to_ns
	$(RM) ../bin/channel_to_ns

install:
	mkdir -p ../bin/
	$(CP) channel_to_ns ../bin/
