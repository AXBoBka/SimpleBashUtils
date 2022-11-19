CC=gcc
CFLAGS=-Wall -Werror -Wextra -std=c11 -D_GNU_SOURCE
SRCS=s21_cat.c
LIB=s21_cat.h

.PHONY: 
	all s21_cat test clean checkcheck check

all:  clean s21_cat

s21_cat: clean
	$(CC) $(CFLAGS) $(SRCS) $(LIB) -o s21_cat

test: all
	bash s21_cat_test.sh

checkcheck: s21_cat
	cppcheck --enable=all --suppress=missingIncludeSystem s21_cat.c s21_cat.h
	CK_FORK=no leaks -atExit -- s21_cat

check: checkcheck clean

clean: 
	rm -rf *.o *.gch *.out log.txt s21_cat
