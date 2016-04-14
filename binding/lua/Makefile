CC = gcc
CFLAGS = -O2 -fPIC -Wall
LUADIR = /usr/local/include
TARGET = protobuf.so

.PHONY : all clean

all : $(TARGET)

$(TARGET) : pbc-lua.c
	$(CC) $(CFLAGS) -dynamiclib -Wl,-undefined,dynamic_lookup -o $@ -I../.. -I$(LUADIR) -L../../build $^ -lpbc

clean :
	rm -f $(TARGET)
