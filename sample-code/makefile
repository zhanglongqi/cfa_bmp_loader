CC=arm-linux-gnueabihf-gcc-4.7
AR=arm-linux-gnueabihf-gcc-ar-4.7
LD=arm-linux-gnueabihf-gcc-4.7

CFLAGS=-Wall -I../src/ -std=c99
LDFLAGS= -L../libs -lcfaf128128b-0145t -lspi-driver -lm

cfa_bmp_loader: main.o ../libs/libspi-driver.a ../libs/libcfaf128128b-0145t.a
	$(LD) main.o -o cfa_bmp_loader $(LDFLAGS)
	#-sshpass -p "root" scp cfa_bmp_loader root@10.10.10.123:/home/root
	
main.o: main.c
	$(CC) main.c -c -o main.o $(CFLAGS)
