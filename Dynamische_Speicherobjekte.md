# Dynamische Speicherobjekte

Der Speicher bleibt hier erhalten, bis er explizit wieder freigegeben wird. 
```
Int *ptr = new int{123};		// erst wird Pointer erzeugt, dieser wird anschließend 						
                            // auf die Speicheradresse des mit new erzeugten 							
                            // Integers initialisiert
```
Fehlt zusammenhängender, ausreichender Speicher, wird eine bad_alloc Exception geworfen.
### Löschen:
```
delete ptr;				// rechts muss ein Zeiger stehen
delete [] ptr;				// soll ein Array gelöscht werden, muss dies angegeben werden
ptr = nullptr;				// Zeiger auf null setzen, da sonst auf zufällige Speicheradresse
```
## Smart Pointer
```
#include <memory>
std::unique_ptr<typ[]>name(new int[i]{0});
name[0] = i				// gewohnte Wertezuweisung
```
