
# The -mno-cygwin option doesn't work with gcc 4
CXX = g++
CC = gcc-3 -mno-cygwin

TARGET = ardpicprog.exe
VERSION = 0.1.2

SOURCES = main.cpp hexfile.cpp serialport.cpp serialport_win.cpp
OBJECTS = hexfile.o main.ovc serialport.o serialport_win.o

CXXFLAGS = -g -Wall -DARDPICPROG_VERSION=\"$(VERSION)\"

LDFLAGS += -g -lstdc++

all:
	$(CXX) $(SOURCES) -o $(TARGET)
	$(TARGET)
	
clean:
	rm -f $(TARGET) $(OBJECTS)

hexfile.o: hexfile.h serialport.h
main.o: serialport.h hexfile.h
serialport.o: serialport.h
serialport_win.o: serialport.h
