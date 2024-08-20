
TARGET := main.exe

OBJS_CPP := $(patsubst %.cpp, %.o, $(wildcard *.cpp))
OBJS_CC := $(patsubst %.cc, %.o, $(wildcard *.cc))
OBJS_C := $(patsubst %.c, %.o, $(wildcard *.c))

CFLAGS := -g -Wall -I./include --std=c++20
LDFLAGS :=  -lpthread


%.o: %.cpp
	g++ $(CFLAGS) $(LDFLAGS) -o $@ -c $^

%.o: %.cc
	g++ $(CFLAGS) $(LDFLAGS) -o $@ -c $^

%.o: %.c
	g++ $(CFLAGS) $(LDFLAGS) -o $@ -c $^

$(TARGET): $(OBJS_CPP) $(OBJS_CC) $(OBJS_C)
	g++ $(CFLAGS) $(LDFLAGS) -o $@ $^

all: $(TARGET)


clean:
	rm -f $(OBJS_CPP) $(OBJS_CC) $(OBJS_C) $(TARGET)


.PHONY: clean all
