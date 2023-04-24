TARGET := display
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

clean:
	rm -f $(TARGET) $(OBJ) $(OBJ2)

