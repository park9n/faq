Q. How could I set-up?
- Build standalone: https://github.com/google/googletest/blob/master/googletest/README.md#standalone-cmake-project
- Link
```
$ sudo ln -s ~/git/googletest/googletest/include/gtest /usr/local/include/gtest
$ sudo ln -s ~/git/googletest/mybuild/lib/libgtest.a /usr/local/lib/libgtest.a
$ sudo ln -s ~/git/googletest/mybuild/lib/libgtest_main.a /usr/local/lib/libgtest_main.a
$ sudo ln -s ~/git/googletest/mybuild/lib/libgmock.a /usr/local/lib/libgmock.a
$ sudo ln -s ~/git/googletest/mybuild/lib/libgmock_main.a /usr/local/lib/libgmock_main.a
```
- Configure Makefile
```
GOOGLE_TEST_INCLUDE = /usr/local/include
GOOGLE_TEST_LIB = gtest

CXX = g++
CXXFLAGS = -std=c++11 -c -Wall -I $(GOOGLE_TEST_INCLUDE)
LD_FLAGS = -L /usr/local/lib -l $(GOOGLE_TEST_LIB) -l pthread

OBJECTS = test.o
TARGET = fizzbuzz

all: $(TARGET)

$(TARGET): $(OBJECTS)
    $(CXX) -o $(TARGET) $(OBJECTS) $(LD_FLAGS)

%.o: %.cpp
    $(CXX) $(G++_FLAGS) $<

clean:
    rm -f $(TARGET) $(OBJECTS)

.PHONY: all clean
```
