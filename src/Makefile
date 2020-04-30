CC=gcc
CCFLAGS += -g -Wall -Wextra

# created to the list
MAIN = rr rw sr sw background
all : $(MAIN)

rr.o : rr.c
	$(CC) $(CCFLAGS) -c rr.c

rr : rr.o
	$(CC) $(CCFLAGS) $^ -o $@ -pthread -lrt

rw.o : rw.c
	$(CC) $(CCFLAGS) -c rw.c

rw : rw.o
	$(CC) $(CCFLAGS) $^ -o $@ -pthread -lrt

sr.o : sr.c
	$(CC) $(CCFLAGS) -c sr.c

sr : sr.o
	$(CC) $(CCFLAGS) $^ -o $@ -pthread -lrt -lm

sw.o : sw.c
	$(CC) $(CCFLAGS) -c sw.c

sw : sw.o
	$(CC) $(CCFLAGS) $^ -o $@ -pthread -lrt -lm

background.o : background.c
	$(CC) $(CCFLAGS) -c background.c

background : background.o
	$(CC) $(CCFLAGS) $^ -o $@

clean :
	rm -rf $(MAIN) *.o
