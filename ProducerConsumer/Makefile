# My third makefile

# Name of the project
BIN=producerConsume

# .c files
C_SOURCE=$(wildcard ./src/*.c)

# .h files
H_SOURCE=$(wildcard ./src/*.h)

# Object files
OBJ=$(subst .c,.o,$(subst src,obj,$(C_SOURCE)))

# Compiler and linker
CC=gcc

# Flags for compiler
CC_FLAGS=-c         \
         -W         \
         -Wall      \
         -ansi      \
         -pedantic

# Command used at clean target
RM = rm -rf

#
# Compilation and linking
#
all: objFolder $(BIN)

$(BIN): $(OBJ)
	$(CC) $^ -o $@

./obj/%.o: ./src/%.c ./src/%.h
	$(CC) $< $(CC_FLAGS) -o $@

./obj/main.o: ./src/main.c $(H_SOURCE)
	$(CC) $< $(CC_FLAGS) -o $@

objFolder:
	@ mkdir -p obj

run:
	@ ./$(BIN)

clean:
	@ $(RM) ./obj/*.o $(BIN) *~
	@ rmdir obj

.PHONY: all clean