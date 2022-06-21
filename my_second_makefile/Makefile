# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: rda-silv <rda-silv@student.42sp.org.br>    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/06/19 17:32:00 by rda-silv          #+#    #+#              #
#    Updated: 2022/06/20 23:04:34 by rda-silv         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# variables
PROJ_NAME=printy

# .c sources (.c files)
C_SRC=$(wildcard *.c)

# h sources (.h files)
H_SRC=$(wildcard *.h)

# object files
OBJ=$(C_SRC:.c=.o)

# compiler
CC=gcc

# flags
CC_FLAGS=-c     \
         -g     \
         -W     \
         -Wall  \
         -Wextra\
         -Werror\
         -ansi  \
         -pedantic

# compilation and linking
all: $(PROJ_NAME)

$(PROJ_NAME): $(OBJ)
		$(CC) -o $@ $^

%.o: %.c %.h
		$(CC) -o $@ $< $(CC_FLAGS)

main.o: main.c $(H_SRC)
		$(CC) -o $@ $< $(CC_FLAGS)

clean: 
		rm -rf *.o $(PROJ_NAME) *~