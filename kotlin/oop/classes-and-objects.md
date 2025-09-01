# Classes and Objects

Kotlin unterstützt OOP mit Klassen, aus denen Objekte erzeugt werden können, die Eigenschaften und verhalten haben.

Eine Klasse
    
    bildet die Vorlage um daraus Objekte zu erzeugen
    definiert welche Methoden (Verhalten) und welche Properties (Eigenschaften) die aus ihr erzeugten Objekte haben

Ein Objekt

    ist eine individuelle Instanz erzeugt aus einer Klasse
    die Klasse entspricht dem Datentyp des Objekts

Die Properties

    entsprechen dem Zustand eines Objekts
    jedes Objekt hat einen eigenen Zustand, auch wenn mehrere Objekte aus derselben Klasse erzeugt wurden  

Die Functions

    entsprechen dem Verhalten eines Objekts
    in Kotlin heissen functions, die zu einer Klasse gehören, member functions

---
1. [Klassendeklaration](#klassendeklaration)
2. [Properties](#proterties)
3. [Klassenarten](#klassenarten)
---

## Klassendeklaration

Eine Klassendeklaration
- wird mit dem Keyword `class` eingeleitet
- gefolgt vom identifier (Name der Klasse resp. des Datentyps)
- gefolgt von einem Class Header mit möglichen `val` oder `var` properties in `()`
- gefolgt von einem Optionalen Class Body in `{}` ebenfalls mit möglichen `val` oder `var` properties 

```kotlin
class Developer(val id: Int, val email: String)
```

```kotlin
class Developer(val id: Int, val email: String) {

    var favouriteLanguage = "Kotlin"
}
```

```kotlin
class Developer(val id: Int, val email: String) {

    var favouriteLanguage: String

    init {
        favouriteLanguage = "Kotlin"
    }

}
```

## Properties

Je nachdem wo und wie ein Property definiert wurde, hat es unterschiedliche Auswirkungen:

### Property mit val oder var im class Header

- Teil des Primärkonstruktors
- Initialisierung direkt durch Konstruktor
- Getter/Setter automatisch generiert
- Keine Komplexe Initialisierung möglich, nur einfache Zuweisungen
- Klassen-Properties, daher von überall innerhalb der Klasse und von ausserhalb (je nach Sichtbarkeit) referenzierbar

### Property mit val oder var im class Body

- Nicht Teil des Konstruktors, sondern unabhängig
- Müssen separat initialisiert werden (direkt bei der Deklaration oder Initialisierungsblock (init) oder in einem Sekundärkonstruktor)
- Getter/Setter automatisch generiert
- Komplexe Initialisierung möglich durch Logik im Initialisierungsblock
- Klassen-Properties, daher von überall innerhalb der Klasse und von ausserhalb (je nach Sichtbarkeit) referenzierbar

### Property ohne val oder var im class Header

- Teil des Primärkonstruktors
- Initialisierung direkt durch Konstruktor
- Keine Getter/Setter, da keine Klassen-Properties
- Keine Komplexe Initialisierung möglich, nur einfache Zuweisungen
- Nur innerhalb des Konstruktors oder des Initialisierungsblocks (init) zugänglich, nach Abschluss der Konstruktionnicht mehr verfügbar

### Property ohne val oder var im class Body

- Nicht Teil des Primärkonstruktors
- Müssen separat initialisiert werden (direkt bei der Deklaration oder Initialisierungsblock (init) oder in einem Sekundärkonstruktor)
- Keine Getter/Setter, da keine Klassen-Properties
- Komplexe Initialisierung möglich, aber nur innerhalb des Scopes
- Nur innerhalb des Scopes gültig, in dem sie deklariert wurden (z. B. in einem Initialisierungsblock, einer Methode oder einem anderen Block).

## Klassenarten

In Kotlin gibt es verschiedene Arten von Klassen und jede Art hat individuelle Eigenschaften.

- [data classes](../data_classes.md)
- [object classes](../object_classes.md)

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Klassen](https://kotlinlang.org/docs/classes.html) 
