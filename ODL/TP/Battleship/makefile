CC       = gcc
RM       = rm
CCFLAGS  = -Wall -Wextra -g
LDFLAGS  = -lcurses -lm
REP_SRC  = ./src/
REP_HEAD = ./headers/
REP_TEST = ./test/
NAME     = battleship
EXEC     = main.o $(REP_HEAD)fonction.o $(REP_SRC)battleship.o $(REP_SRC)fonction.o

$(NAME) : $(LDFLAGS) $(EXEC)
	$(CC) main.c -o $(NAME) $(LDFLAGS) -g

$(REP_HEAD)fonction.o : $(REP_HEAD)fonction.h
	$(CC) -g $(CCFLAGS) -c $<

$(REP_SRC)battleship.o : $(REP_SRC)battleship.c
	$(CC) -g $(CCFLAGS) -c $<

$(REP_SRC)fonction.o : $(REP_SRC)fonction.c
	$(CC) -g $(CCFLAGS) -c $<

clean :
	-@$(RM) *.o
	-@$(RM) battleship
