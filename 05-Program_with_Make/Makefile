# Default rule to build the target
all: random_main

# Link object files to create the executable
random_main: random_main.c
	gcc -o random_main \
			random_main.c \
			random.c \
			-lm

# Clean up build files
clean:
	rm -f random_main

