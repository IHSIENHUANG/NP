all: ftp
	
srv = b023040001_srv.o
cli = b023040001_cli.o
fhuff = b023040001_huffman.o

ftp: b023040001_main.c $(srv) $(cli) $(fhuff)
	gcc -o b023040001_ftp  b023040001_main.c $(srv) $(cli) $(fhuff) -lm
test: b023040001_huffman.o
	gcc -o Test test.c $(fhuff) -lm

b023040001_srv.o: b023040001_srv.c
	gcc -c b023040001_srv.c
b023040001_cli.o: b023040001_cli.c
	gcc -c b023040001_cli.c
b023040001_huffman.o:
	gcc -c b023040001_huffman.c
clear:
	rm -f b023040001_ftp *.o Test *_table
