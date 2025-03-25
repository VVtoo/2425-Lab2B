# Per maggiori informazioni sul comando make:
#     http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/
# Sulle variabili automatiche vedere:
#     https://www.gnu.org/software/make/manual/html_node/Automatic-Variables.html
 
# definizione del compilatore e dei flag di compilazione
# che vengono usati dalle regole implicite
CC=gcc
CFLAGS=-std=c11 -Wall -O -g
LDLIBS=-lm

EXECS=scrivi_primi_bin leggi_bin scrivi_primi_sc write_speed matrice 

all: $(EXECS)

scrivi_primi_bin: scrivi_primi_bin.c
	$(CC) $(CFLAGS) -o $@ $< $(LDLIBS)

leggi_bin: leggi_bin.c
	$(CC) $(CFLAGS) -o $@ $< $(LDLIBS)

scrivi_primi_sc: scrivi_primi_sc.c
	$(CC) $(CFLAGS) -o $@ $< $(LDLIBS)

write_speed: write_speed.c
	$(CC) $(CFLAGS) -o $@ $< $(LDLIBS)

matrice: matrice.c
	$(CC) $(CFLAGS) -o $@ $< $(LDLIBS)

clean:
	rm -f $(EXECS)
		
		
