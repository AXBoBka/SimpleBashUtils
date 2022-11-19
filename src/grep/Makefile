CC=gcc
CFLAGS=-std=c11 -Wall -Werror -Wextra -std=c11 -D_GNU_SOURCE
SOURCES=s21_grep.c

s21_grep: clean $(SOURCES)
	$(CC) $(CFLAGS) $(SOURCES) -o s21_grep

test: s21_grep
	bash s21_test_grep.sh

clean:
	rm -rf s21_grep RESULT_VALGRIND.txt log.txt