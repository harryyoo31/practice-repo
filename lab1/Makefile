cxx = g++
flag = -g -Wall -std=c++17 -I/opt/homebrew/include
link_gtest = -L/opt/homebrew/lib -lgtest -lgtest_main -pthread

all: test

run: test
	./test

library.o: library.cpp library.hpp
	$(cxx) $(flag) library.cpp -c -o library.o

test: test.cpp library.o
	$(cxx) $(flag) test.cpp library.o $(link_gtest) -o test

.PHONY: clean
clean:
	rm *.o test
