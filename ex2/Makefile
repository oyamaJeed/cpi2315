TARGET := test2
SRC := $(TARGET).c
OBJ := $(TARGET).o
OBJ2 := libdlink.so

CFLAGS := -g -Wall
LFLAGS := -lm -pthread
CC := gcc $(CFLAGS) $(LFLAGS)


all : $(OBJ) $(OBJ2)

.c.o:
	$(CC) -c $^
$(OBJ2) :
	gcc -shared display.c -fPIC -o libdlink.so
	export LD_LIBRARY_PATH="/home/meit2315/cpi2315/ex2"
	gcc -o test2 test2.c -L. -ldlink

clean:
	rm -f $(TARGET) $(OBJ) $(OBJ2)

