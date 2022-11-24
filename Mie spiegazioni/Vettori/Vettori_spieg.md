# :dizzy: <br /> Vettori

### Che cosa sono?

###### **I vettori** sono dei **contenitori** proprio come gli array, ma hanno un grande vantaggio, la loro grandezza è **dinamica** *(gli array sono statici e non possono cambiare la loro grandezza nel corso della esecuzione del codice)* ma i loro vantaggi non finiscono qui, hanno un'altro punto al favore, quello di poter lavorare con essi attraverso le **funzionalità** apposite e **puntatori**, rendendoci la vita più semplice e permettendoci di finire i lavori in pochi istanti. Grazie alla loro grandezza dinamica usano la memoria in una maniera più **efficace**.


### Come riempire un vettore <br />

I modi in cui si può riempire un vettore sono **numerosi**, uno dei *più diffusi* è quello con iterazione mediante il ciclo **FOR**, innanzitutto per poter **lavorare** con gli vettori bisogna **includere** il *HEADER vector*!


#### Con il ciclo for (utente)

```cpp
vector <tipo int, char, double, short int...> nome_del_vettore;
	
	int numero = 0, n = 5;
	
	for (int i = 0; i < n; ++ i) {
		
		cin >> numero;
		
		nome_del_vettore.push_back(numero);
	}
```

###### Spiegazione

`vector <int> nome_del_vettore;` con questa stringa del codice creiamo un vettore di tipo int (non per forca dev'essere di topo int, può essere di tipo char, double... e cet.)

`for (int i = 0; i < n; ++ i)` con questa stringa creiamo un semplice ciclo for

`cin >> numero;` prendiamo dal utente un valore, in questo caso di tipo int (un numero)

`nome_del_vettore.push_back(numero);` con il **.push_back** assegnamo il nostro valore all'**ultima** posizione del vettore! quel puntino è molto importante è un puntatore, **non scordatevelo**!


#### Con la funzione fill

```cpp
fill (nome_del_vettore.begin() + 1, nome_del_vettore.end() - 3, 4);
```

Il nostro vettore è stato riempito di valore 4 in seguente modo: `0 4 4 4 4 0 0 0`

###### Spiegazione

`(nome_del_vettore.begin(), nome_del_vettore.end()` creiamo un range che va dal inizio (0) alla fine fine (x) in questo caso il nostro vettore deve avere una grandezza inizializzata lo si fa in questo modo: ```cpp vector <int> nome_del_vettore (la_sua_grandezza);``` in questo caso la grandezza del vettore è pari a 8!

`+ 1    - 3, 4` grazie ai questi li ho chiamati "parametri" possiamo riempire ad esempio soltanto il centro del vettore, ovvero con il + 1 si lascia lo spazio al valore (0 = niente) e si inizia a riempire il vettori di valore 4 ma grazie al - 3 i valori verranno riempiti soltanto dal 2 a 5

``