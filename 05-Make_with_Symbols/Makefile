# Compiler to use
CC = gcc

# Compiler flags:
# -Wall: Enable all warning messages
# -Wextra: Enable extra warning flags
# -g: Include debugging information
CFLAGS = -Wall -Wextra -g

# Target executable name
TARGET = hello

# Source files
SRCS = hello.c

# Object files (replace .c with .o)
OBJS = $(SRCS:.c=.o)

# Default rule to build target
all: $(TARGET)

# Link object files to create the executable
$(TARGET): $(SRCS)
	$(CC) $(CFLAGS) -o $(TARGET) $(SRCS)

# Clean up build files
clean:
	rm -f $(OBJS) $(TARGET)
