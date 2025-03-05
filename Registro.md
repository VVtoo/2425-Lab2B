##  Introduzione ad array, puntatori e file (introC)


**Lezione 1** (17/9/24)

Introduzione al linguaggio C. Esempio di lettura e scrittura di interi dal terminale. Compilazione: errori e warning. Permessi di lettura scrittura esecuzione `rwx`. Esecuzione di programmi. Array "statici" (tipo `int a[n]` in `somma.c`) vs array "dinamici" gestiti con `malloc/free` utilizzati in `sommad.c`

-----------------------

**Lezione 2** (20/9/24)

* Allocazione dinamica di array in C. Funzioni: malloc/free/realloc. Programma `primi.c`.
* Utilizzo di *valgrind* per verificare il corretto utilizzo e deallocazione degli array

-------

**Lezione 3** (24/9/24)

* Introduzione ai puntatori; uso di puntatori negli array.
* Significato e uso di `*` e `&`
* Esempio passaggio parametri per riferimento attraverso un puntatore: `parametri.c` e `sommadprod.c`
* Significato istruzioni `#include`

-------

**Lezione 4** (27/9/24)

* Warning di valore ignorato. Comando `man`, sezioni del manuale, 
* Rappresentazione di stringhe in C: i tipi `char` e `char *`. Stampa di stringhe con `printf`, calcolo lunghezza con `strlen`. 
* Uso dei parametri argc/argv di main()
* Copia di un puntatore vs copia degli elementi di un array: la funzione strdup()


-------

**Lezione 5** (1/10/24)

* Introduzione al *makefile*; compilazione con il comando *make*
* Scrittura in un file di testo: fopen(), fprintf(), fclose(). Modalità append.
* Comandi `less` e `od` per visualizzare il contenuto di un file
* Lettura da un file di testo: comando fscanf().  
* Terminazione in caso di errori: funzione perror(). Cenni sulla ridirezione di `stdout`

-------

**Lezione 6** (4/10/24)

* Passaggio di array dalle/alle funzioni
* Uso di `assert`
* stdout/stderr e loro ridirezione; esempi
* Esercitazione sulle stringhe e sul passaggio di array alle funzioni. Significato del tipo `const char *`


-------


**Lezione 7** (8/10/24)


* Equivalenza fra `*a` e `a[0]`
* Equivalenza fra `a` e `&a[0]`, significato di `&a[i]`
* Aritmetica dei puntatori: definizione di `a+i` come `&a[i]`
* Esempio di uso della notazione `&a[i]` nel *mergesort*
* Creazione e deallocazione di un array di stringhe, programma `astringhe`
* Lettura di stringhe con `scanf`:  problematica del [buffer overflow](https://en.wikipedia.org/wiki/Buffer_overflow)

----

**Lezione 8** (15/10/24)


* Lettura di stringhe con `scanf`: evitare il buffer overflow: modificatori `%Ns` (con N massimo numero di caratteri) e `%ms`
* Costruzione/concatenazione di stringhe mediante `asprintf` 
* Definizione di tipi composti con `struct`; definizione di nuovi tipi con `typedef` e uso combinato con `struct`
* Operazioni sui tipi composti, notazioni `.` e  `->`; passaggio per valore e per riferimento di struct. 
* Ordinamento di un array di struct mediante mergesort



## Definizione di streuct: liste e alberi binari di ricerca (02struct)

**Lezione 9** (18/10/24)

* Array di puntatori a struct, esempio: array di capitali. Confronto lessicografico di stringhe, funzione `strcmp`.
* Ordinamento array di puntatori a struct mediante mergesort
* Terminazione in caso di errori: funzione perror() e variabile globale `errno`


----

**Lezione 10** (22/10/24)

* Introduzione all'uso delle funzioni come parametri di altre funzioni
* Mergesort con funzione di confronto passata come argomento
* Esercizi: ordinamento di file per dimensione e nome. Funzioni `fseek` e `ftell`. Uso del tipo `long`


----


**Lezione 11** (25/10/24)


* Introduzione alla funzione di libreria  `qsort`
* Prova in itinere sugli argomenti delle lezioni 1-9. 


----

**Lezione 12** (29/10/24)

* Puntatori generici (`void *`). Tipo della funzione di confronto in `qsort`, casting.
* Introduzione alle *linked list*: creazione, stampa, distruzione di liste. Inserimento in testa e in coda. 


----

**Lezione 13** (4/11/24)

* Linked list: procedure ricorsive per la cancellazione e l'inserimento ordinato. 
* Alberi binari di ricerca: procedure ricorsive per costruzione, visita e deallocazione.  

--- 

**Lezione 14** (5/11/24)

* Alberi binari di ricerca: visita in preorder, ricerca di un elemento, calcolo altezza (file `abr_capitali.c`)
* Lettura da file con getline(). Parsing di stringhe mediante strtok() (file `leggicitta.c`)



## Assembler ARM (03assembler)


**Lezione 15** (8/11/24)

* Variabili statiche. Funzionamento interno di strtok(). Esempio di lettura di stringhe mediante strtok() (`legginomi.c`)
* Test di primalità in assembler ARM (`primo.s`). Makefile e compilazione di programmi formati da più file. Concetto di target, prerequisiti e comandi. 
* Uso di un debugger: esecuzione passo/passo, breakpoint, visualizzazione variabili locali. 
* Accesso a sistemi remoti via ssh con X11 forwarding. Uso di gdbgui per debugging su sistemi remoti attraverso un browser.

---


**Lezione 16** (12/11/24)

* File oggetto (`.o`) e compilazione separata; makefile con target multipli. 
* Implementazione `strcmp` in assembler ARM.
* Breakpoint condizionali in gdb/gdbgui. Visualizzazione registri ARM e loro uso nei breakpoint condizionali.

--- 

**Lezione 17** (13/11/24)

* Ancora sul makefile: lazy evaluation, variabili, variabili automatiche, e regole implicite.
* Operatori bitwise `&`, `|`, `^`, `~`, `<<`, `>>`. Esempio: `bitops.c`
* Utilizzo di puntatori e costruzione di un array di numeri primi in assembler ARM (`array_primi.s`)



## Utilizzo di file binary (04fileBinary)


**Lezione 18** (19/11/24)

* Esercizi su ABR.
* Definizione e uso di matrici bidimensionali definite in modo statico (ad esempio `int a[3][5]`).


---- 


**Lezione 19** (22/11/24)

* Definizione e uso di matrici bidimensionali definite in modo dinamico come array di righe.
* Seconda prova in itinere.


----

**Lezione 20** (26/11/24)

* Lettura e scrittura di file binari in C: funzioni `fread` e `fwrite`; comando `od`.
* System calls vs library functions.
* Sezioni del system manual (comando man).
* Esempi: open/read/write vs fopen/fread/fwrite/fprintf




## Utilizzo di classi e collezioni in Java (05java)


**Lezione 21** (29/11/24)

* Permessi dei file e notazione ottale in `open`. Significato e uso di `umask(1)` e `chmod(1)`
* Esempio prestazioni di `write(2)` vs `fwrite(3)`.
* Introduzione a Java: la classe `Coppia`, overloading dei metodi `toString` e  `equals`, la classe `ArrayList<>`, metodi `sort` e `contains`


----


**Lezione 22** (3/12/24)

Java: la classe `HashSet` e il metodo `hashCode`. Lettura da file con `BufferedReader` e `FileReader`.
Uso di eccezioni (checked e unchecked).
Cenni sulla gerarchia delle collezioni: `Set` vs `HashSet` vs 'LinkedHashSet', `List` vs `ArrayList` vs `LinkedList`.
La classe `TreeSet` e l'interfaccia `Comparable`. Uso dell'annotazione `@Override`

----

**Lezione 23** (10/12/24)

Java: classi (astratte) e interfacce; differenza di uso fra `extends` e `implements`.
Classe `Grafo`, cammini minimi con algoritmo di Dijkstra. Classe `LogGrafo` 
e implementazione di un grafo di città mediante l'interfaccia `Nodo` (si veda il `main` della classe `GrafoCitta`)
Cenni sull'uso di  [`javadoc`](https://en.wikipedia.org/wiki/Javadoc)



## Uso di Python per interagire con il file system 



**Lezione 24** (28/1/25)

Introduzione a Python, differenze e similarità con il C. 
Sintassi, interprete, istruzioni `if`, `else`, `elif`, `for`, `while`. Definizione di funzioni e Docstring. Liste e tuple.


---

**Lezione 25** (30/1/25)

Python: interprete ed esecuzione dalla linea di programma. 
Dizionari: funzionamento interno e vincoli sulle chiavi.  
Esempio: costruzione classifica leggendo risultati da file. Uso di `import` e `sys.argv`. Apertura di file con `with` e `open`. Istruzione `raise` per segnalare gli errori. Sorting di liste utilizzando una key function. 
Esercizi per casa: *Ribalta file* e *Ordina file*

---

**Lezione 26** (4/2/25)

Definizione e uso di classi in python. I metodi speciali `__init__`,  ` __str__`, `__repr__` e ,  `__lt__`.
Uso del decorator `@functools.total_ordering`.
Esplorazione del filesystem in Python: metodi dei moduli `os` e `os.path`.  Concetto di [link symbolici](https://linuxize.com/post/how-to-create-symbolic-links-in-linux-using-the-ln-command/). 


---

**Lezione 27** (6/2/25)

Sottoclassi in python. Metodi speciali per operatori aritmetici (`__add__`, `__mul__`, etc.). Metodi `__eq__` e `__hash__`. 
Ancora sull'esplorazione del filesystem in Python, [permessi](https://linuxcommand.org/lc3_lts0090.php) associati alle directory.
Creazione di elenco dei file ordinato per dimensione decrescente


---

**Lezione 28** (11/2/25)

Istruzione `type` all'interno del metodo `__eq__`
Invocazione comandi della shell da python con `subprocess.run`.
Ricerca di file duplicati in python utilizzando il comando della shell  `cmp`. 
Utilizzo della classe `Miofile` per memorizzare le informazioni relative a un singolo file.


---

**Lezione 29** (13/2/25)

Parametri posizionali e keyword. Uso di `*` e `**` per funzioni con numero arbitrario di parametri.
Ancora su esplorazione del filesystem: ricerca basata sul tempo di ultima modifica e uso di espressioni regolari.

---

**Lezione 30** (18/2/25)

Introduzione ai thread in C. 
Esercitazione in aula su python (testo disponibile su moodle). 



---

**Lezione 31** (20/2/25)

Ancora sui thread in C. Uso di mutex.  
Prova in itinere sull'uso di python per l'esplorazione del filesystem (testo disponibile su moodle).


Nota: potete osservare che il prototipo della funzione `pthread_mutex_init` contiene il modificatore `restrict`. Si tratta di un modificatore riferibile ai puntatori che se usato permette al compilatore di generare del codice più efficiente. Potete trovare ulteriori dettagli ed esempi su [stack overflow](https://stackoverflow.com/questions/745870/realistic-usage-of-the-c99-restrict-keyword).



----

**Lezione 32** (25/2/25)

Uso delle funzioni in `xerrori.c` per la gestione degli errori, compresa la relativa impostazione del `makefile`.
Semafori  e loro uso per implementare la tecnica produttori e consumatori.


----

**Lezione 33** (27/2/25)

Altri esempi di uso dei semafori. Esercitazione in aula sul sorting parallelo


----

**Lezione 34** (4/4/25)


Uso di `pthread_barrier`, compilazione condizionale con `#if/#else/#endif`.
Uso di target multipli nel makefile, e definizione di costanti dalla linea di comandi 
(vedi uso di `-D USE_BARRIER` per ottenere `primi_barrier.o`)
Soluzione esercitazione del 27/2 sul sorting parallelo.

---


**Lezione 35** (6/4/25)
