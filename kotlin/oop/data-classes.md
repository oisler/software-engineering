# Data classes

Datenklassen sind Klassen, die mit dem `data`-Keyword deklariert werden und dadurch besondere Eigenschaften haben.<br>
Bestimmte Member-Funktionen werden vom Compiler automatisch generiert:
- equals()
- hashCode()
- toString()
- copy()
- componentN()-Funktionen (für Destrukturierung)

Für diese Automatische Generierung von Member functions müssen folgende Regeln eingehalten werden:
- Der Primary Constructor muss mindestens einen Parameter haben
- Alle Primary Constructor-Parameter müssen mit `val` oder `var` deklariert sein
- Datenklassen können nicht abstract, open, sealed oder inner sein

Deshalb eignen sie sich besonders für DTOs oder grundsätzlich Datenmodell-Klassen

## Veränderbarkeit

Eine Instanz von Person ist immutable, weil alle Properties mit `val` deklariert sind.<br>
D.h. name und age können nach der Initialisierung nicht mehr verändert werden.<br>
**Wichtig:**

    data classes sind nicht automatisch immutable.
    Die Mutabilität hängt davon ab, ob die Properties mit val (immutable) oder var (mutable) deklariert werden.


```kotlin
data class ImmutablePerson(val name: String, val age: Int)

fun main() {
    val person = ImmutablePerson("Alice", 25)
    person.name = "Bob" // Änderung unmöglich
}
```
    
```kotlin
data class MutablePerson(var name: String, var age: Int)

fun main() {
    val person = MutablePerson("Alice", 25)
    person.name = "Bob" // Änderung möglich
}
```

- eine Instanz von Person ist immutable, d.h. name und age können nach erstmaliger initialisierung nicht mehr verändert werde
- die Mutabilität wird nicht durch die `data class` selbst vorgegeben, sondern durch die Wahl von `val` für die Properties

## Kopieren

Die `copy()`-Funktion ermöglicht es, eine Kopie eines Objekts zu erstellen, wobei einzelne Properties geändert werden können.

```kotlin
val person1 = ImmutablePerson("Alice", 25)
val person2 = person1.copy(age = 30)

println(person1) // Ausgabe: Person(name=Alice, age=25)
println(person2) // Ausgabe: Person(name=Alice, age=30) -> neue Instanz
```

## Destrukturierung

Data classes unterstützen Destrukturierung, damit lassen sich die Properties eines Objekts einfach in einzelne Variablen zerlegen:

```kotlin
val person = Person("Alice", 25)
val (name, age) = person

println(name) // Ausgabe: Alice
println(age)  // Ausgabe: 25
```

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Data classes](https://kotlinlang.org/docs/data-classes.html) 
