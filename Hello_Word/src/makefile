
HEADER_DIR = ../include

SRC = $(wildcard *.c)
INC = $(wildcard *.h)
LIB_DIR = ../lib 

OBJ = $(patsubst %.c, %.o, $(SRC))

CC = /usr/bin/gcc
CFLAGS = -I$(HEADER_DIR)
CFLAGS += -g -O2 -Wall -Werror -Wno-unused
LDFLAGS = -L$(LIB_DIR)
LIBS = -lpthread

TARGET := helloWorld

$(TARGET):$(OBJ)
	@echo "开始编译"
	$(CC) $< -o $@ $(LDFLAGS) $(LIBS)
	cp $@ ../bin
	@echo "编译结束"
$(OBJ):$(SRC)
	$(CC) -c $(CFLAGS) $^ -o $@

.PHONY:clean

clean:
	rm $(OBJ) $@

