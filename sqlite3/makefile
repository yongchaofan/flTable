HEADERS = sqlite3.h
CC=gcc

all: sqlite3.o

%.o: %.c
	${CC} -Os 	-DSQLITE_OMIT_DECLTYPE -DSQLITE_OMIT_DEPRECATED \
				-DSQLITE_OMIT_PROGRESS_CALLBACK \
				-DSQLITE_DEFAULT_MEMSTATUS=0 \
				-DSQLITE_DEFAULT_WAL_SYNCHRONOUS=1 \
				-DSQLITE_LIKE_DOESNT_MATCH_BLOBS \
				-DSQLITE_MAX_EXPR_DEPTH=0 -DSQLITE_USE_URI\
				-c $< -o $@

clean:
	rm "sqlite3.o"