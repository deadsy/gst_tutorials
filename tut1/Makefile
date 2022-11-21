
CC = gcc

OUT = tut1

SRC = basic-tutorial-1.c

OBJ = $(patsubst %.c, %.o, $(SRC))

LIBS = `pkg-config --libs gstreamer-1.0`

CFLAGS = -Wall -Wstrict-prototypes -Werror
CFLAGS += `pkg-config --cflags gstreamer-1.0`

.c.o:
	$(CC) $(CFLAGS) $(INC) -c $< -o $@

all: $(OUT)

$(OUT): $(OBJ)
	$(CC) -o $(OUT) $(OBJ) $(LIBS)

clean:
	-rm $(OBJ)
	-rm $(OUT)
