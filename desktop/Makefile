CC = cc
CFLAGS = -Wall -Wextra -O2 -I../components/sim
SIM = ../components/sim/fluid.c

sim: main.c $(SIM) ../components/sim/fluid.h
	$(CC) $(CFLAGS) -o sim main.c $(SIM) -lm

test: ../test/test_sim.c $(SIM) ../components/sim/fluid.h
	$(CC) $(CFLAGS) -g -fsanitize=address,undefined -o test_sim ../test/test_sim.c $(SIM) -lm
	./test_sim

clean:
	rm -f sim test_sim *.ppm

.PHONY: test clean
