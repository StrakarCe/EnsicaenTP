# ENSICAEN
# 6 Boulevard Marechal Juin
# F-14050 Caen Cedex
#
# This file is owned by ENSICAEN students.
# No portion of this document may be reproduced, copied
# or revised without written permission of the authors.
#
# @author Florian DUVAL <florian.duval@ecole.ensicaen.fr>
# @version 0.0.1 – 2017-09-29
#
# @todo the list of improvements suggested for the file.
# @bug the list of known bugs.

CC       = gcc
RM       = rm
CCFLAGS  = -Wall
LDFLAGS  = -lcurses -lm
REP_SRC  = src/
REP_HEAD = include/
REP_TEST = test/
REP_OBJ  = obj/
REP_BIN  = bin/
NAME     = battleship
EXEC     = $(REP_OBJ)main.o $(REP_OBJ)fonction.o $(REP_OBJ)$(NAME).o

$(NAME) : $(LDFLAGS) $(EXEC)
	$(CC) $(EXEC) -o $(REP_BIN)$(NAME) $(LDFLAGS) -g

$(REP_OBJ)main.o : main.c
	$(CC) $(CCFLAGS) -c $<

$(REP_OBJ)$(NAME).o : $(REP_SRC)$(NAME).c
	$(CC) $(CCFLAGS) -c $<

$(REP_OBJ)fonction.o : $(REP_SRC)fonction.c
	$(CC) $(CCFLAGS) -c $<

clean :
	-@$(RM) $(REP_OBJ)*.o
	-@$(RM) $(NAME)
