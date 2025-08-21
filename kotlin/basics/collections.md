# Collections

Eine Sammlung enthält eine Anzahl von Objekten, die vom gleichen Typ (oder einem Subtyp davon) sind.<br>
Eine Sammlung kann auch leer sein. d.h. sie enthält noch keine Elemente, wurde aber bereits deklariert.<br>

In Kotlin gibt es drei Haupttypen von Sammlungen:
1. Listen (Lists)
2. Mengen (Sets)
3. Maps

## Lists

- Eine Liste ist eine geordnete Sammlung von Elementen
- Elemente werden in der Reihenfolge gespeichert, in der sie hinzugefügt werden
- Doppelte Elemente sind erlaubt
- Auf ein Element in einer Liste kann über den Indexzugriffsoperator ([]) zugegriffen werden. Beispiel: myList[0] gibt das erste Element der Liste zurück

## Sets
- Ein Set ist eine ungeordnete Sammlung von Elementen
- Keine Duplikate erlaubt – nur eindeutige Elemente können enthalten sein
- Auf ein Element kann nicht über einen bestimmten Index zugegriffen werden, da es keine Reihenfolge gibt

## Maps

- Eine Map speichert Elemente als Schlüssel-Wert-Paare
- Jeder Schlüssel in einer Map muss eindeutig sein, damit Kotlin weiss, welchen Wert abrufen werden soll
- Es können doppelte Werte in einer Map vorkommen, solange sie unterschiedliche Schlüssel haben.
- Auf ein Element in einer Map kann über den Schlüssel mit dem Indexzugriffsoperator ([]) zugegriffen werden. Beispiel: myMap["key"] gibt den Wert zurück, der dem Schlüssel "key" zugeordnet ist.

## Zusätzliche Hinweise
- Jeder Collection-Typ kann entweder veränderbar (mutable) oder nur-lesbar (read-only) sein. 
- Read-only bedeutet, dass keine Elemente hinzugefügt oder entfernt werden können
- Mutable bedeutet, dass du der Sammlung Elemente hinzugefügt oder entfernt werden können
- Um ungewollte Änderungen zu verhindern, kann eine read-only View veränderbaren Sammlung erstellt werden

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Collections](https://kotlinlang.org/docs/collections-overview.html) 
