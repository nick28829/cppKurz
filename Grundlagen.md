# Grundlagen
### Grundgerüst:
```
#include <iostream>		// Verwenden von Bibliotheken
#include “file.h”		// Verwenden von Header-Files

int main(){
	…
	return 0;
}
```

Operatoren: +, -, *, /, %
Kurzschreibweise: +=, -=, *=, /=
Verknüpfungen: &&, ||, !
Bitweise Verknüpfungen: &, |, ^,~
Vergleichsoperatoren: ==, !=, <=, >=, <, >
Inkrementor: a++, ++a, a--, --a

### Ausgabefunktionen:



### Schlüsselworte:

const: unveränderlicher Wert, innerhalb einer Klasse darf er nur vom Konstruktor einmalig geschrieben werden, kann auch auf Objekte angewendet werden, const Objekte dürfen nicht als Pointer verwendet werden (also this→). Const-Funktionen dürfen nicht schreiben (void func() const{}). Const typ func() hingeben gibt einen const Wert zurück

public: Eigenschaften können überall aufgerufen werden

protected: Eigenschaften können nur innerhalb der Klasse aufgerufen werden

private: ähnlich protected, aber nach Vererbung nicht mehr aufrufbar

auto: wird verwendet, um den Typ einer Variablen automatisch zuzuweisen

extern: wird für Variable verwendet, die in einem anderen Modul definiert ist
