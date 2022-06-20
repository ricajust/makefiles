# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: rda-silv <rda-silv@student.42sp.org.br>    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/06/19 17:32:00 by rda-silv          #+#    #+#              #
#    Updated: 2022/06/19 17:44:17 by rda-silv         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# variables
PROJ_NAME=printy

# .c sources (.c files)
C_SRC=$(wildcard *.c)

# h sources (.h files)
H_SRC=$(wildcard *.h)

# object files
OBJ=$(C_SRC=.c=.o)

# compiler
CC=gcc

# flags
CC_FLAGS=-c	\
		 -W	\

all: printy

printy: main.o helloworld.o
		gcc -o printy main.o helloworld.o

main.o: main.c helloworld.h
		gcc -o main.o main.c -c -W -Wall -ansi -pedantic

helloworld.o: helloworld.c helloworld.h
		gcc -o helloworld.o helloworld.c -c -W -Wall -ansi -pedantic

clean: 
		rm -rf *.o *~printy