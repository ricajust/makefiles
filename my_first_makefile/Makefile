# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: rda-silv <rda-silv@student.42sp.org.br>    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/06/19 16:01:01 by rda-silv          #+#    #+#              #
#    Updated: 2022/06/19 16:57:19 by rda-silv         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

all: printy

printy: main.o helloworld.o
		gcc -o print main.o helloworld.o

main.o: main.c helloworld.h
		gcc -o main.o main.c -c -W -Wall -ansi -pedantic

helloworld.o: helloworld.c helloworld.h
		gcc -o helloworld.o helloworld.c -c -Wall -ansi -pedantic

clean:
		rm -rf *.o *~printy