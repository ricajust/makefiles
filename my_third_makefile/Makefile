# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: rda-silv <rda-silv@student.42sp.org.br>    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/06/20 23:08:21 by rda-silv          #+#    #+#              #
#    Updated: 2022/06/20 23:42:39 by rda-silv         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# name fo the project
PROJ_NAME=printy

# .c files
C_SRC=$(wildcard ./src/*.c)

# .h files
H_SRC=$(wildcard ./src/*.h)

# object file
OBJ=$(subst .c,.o,$(subst src,obj,$(C_SRC)))

# compiler and linker
CC=gcc

# flags for compiler
CC_FLAGS=-c      \
         -g      \
         -W      \
         -Wall   \
         -Wextra \
         -Werror \
         -ansi   \
         -pedantic

# command used at clean target
RM=rm -rf

# compilation and linking
all: objFolder $(PROJ_NAME)

$(PROJ_NAME): $(OBJ)
		@echo 'Building binary using GCC Linker: $@'
		$(CC) $^ -o $@
		@echo 'Finished building binary: $@'
		@echo ' '

./obj/%.o: ./src/%.c ./src/%.h
		@ echo 'Building target using GCC Compiler: $<'
		$(CC) $< $(CC_FLAGS) -o $@
		@ echo ' '

./obj/main.o: ./src/main.c $(H_SRC)
		@ echo 'Building target using GCC Compiler: $<'
		#(CC) $< $(CC_FLAGS) -o $@
		@ echo ' '

objFolder:
		@ mkdir -p obj

clean:
		@ $(RM) ./obj/*.o $(PROJ_NAME) *~
		@ rmdir obj

.PHONY: all clean
		