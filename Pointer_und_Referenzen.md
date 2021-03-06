# Referenzen und Pointer
Referenzen sind neue Namen für ein bestehendes Speicherobjekt, also ein Alias für eine Variable. Sie werden wie folgt deklariert:
```
int a = 2; 		// Deklaration einer Variablen
int& a_ref = a		// Erstellung einer Referenzen
int &a_ref = a		// alternative Schreibweise 
```
Referenzen können nur einmal an ein Objekt gebunden werden. Bei erneuter versuchter Zuweisung wird das Speicherobjekt verändert.

Referenzen können auch an Funktionen übergeben werden. So wird verhindert, dass das Objekt bei Funktionsaufruf kopiert wird.
```
Int func(int &var){...}		// Call by reference vs. Call by value
```
Bei Verwendung von Referenzen als Rückgabewert einer Funktion ist darauf zu achten, dass die entsprechenden Objekte keine lokalen Variablen der Funktion sind, da die Referenz sonst nach beenden der Funktion auf ein leeres Element zeigt.

Pointer speichern den Datentyp und den Speicherort eines Objekts. Sie werden wie folgt erzeugt:
```
int *ptr {nullptr};		// mit Nullpointer initialisiert (auch 0, 0L)
int val = 123;
ptr = &val;			// & ist der Addressoperator
```
Bei Ausgabe des Pointer wird die Addresse des Speicherobjekts ausgegeben, bei Verwendung des Addressoperators die Addresse des Pointers.
Zum Zugriff auf den Wert des referenzierten Objekts wird der Indirektionsoperator (auch Verweisoperator) * genutzt.
```
int val = 123;
int *ptr =&val	;
*ptr = 124
std::cout << *ptr << std::endl;
```
*Ausgabe: 124*

Zeiger sollten auf Fehler geprüft werden, etwa ob sie auf ein leeres Objekt zeigen. Dazu dient der Vergleich ptr == nullptr.

Bei Pointern, die auf Objekte einer Klasse zeigen, gilt folgende Syntax
```
Kreis kleinerKreis {25};		// Objekt der Klasse Kreis wird erzeugt
Kreis *ptr = &kleinerKreis;		// Pointer auf das Objekt wird erzeugt
std::cout << ptr -> flaeche();		// mithilfe von -> kann auf Eigenschaften und Methoden des 					// referenzierten Objekts zugegriffen werden
```
Bei C-Arrays ist das Array ein Pointer auf das erste Element:
```
float arr[10];
float *ptr = arr;			// ohne Addressoperator, da Pointer
```
