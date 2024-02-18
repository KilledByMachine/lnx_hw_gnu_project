# Check the value of METHOD environment variable
ifdef METHOD
    ifeq ($(METHOD),1)
        include make1.mk
        include make2.mk
        include make3.mk
    else
        all: main
    endif
else
    all: main
endif

main.o: main.c
    gcc -c -o $@ $<

main: main.o
    gcc -o $@ $^

clean:
    rm -f main main.o
