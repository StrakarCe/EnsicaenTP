CC       = gcc
RM       = rm
CCFLAGS  = -Wall -Wextra -g
LDFLAGS  = -lcurses -lm
EXEC     = main.o headers/fonction.o src/battleship.o src/fonction.c

battleship : $(LDFLAGS) $(EXEC)
	$(CC) main.c -o battleship $(LDFLAGS) -g

headers/fonction.o : fonction.h
	$(CC) -g $(CCFLAGS) -c $<

src/battleship.o : battleship.c
	$(CC) -g $(CCFLAGS) -c $<

src/fonction.o : fonction.c
	$(CC) -g $(CCFLAGS) -c $<

clean :
	-@$(RM) *.o
	-@$(RM) battleship
