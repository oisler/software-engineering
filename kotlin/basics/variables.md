# Variables

Eine Variable ist ein Container zum Speichern von Informationen. Eine Variable

    - speichert Informationen eines definierten Datentyps
    - wird einmal deklariert und kann anschliessend beliebig oft ausgelesen werden

## Declaration

Um eine Variable zu erstellen, braucht es verschiedene Informationen:

- `val` oder `var` ist das Keyword, um die Deklaration einer Variable einzuleiten
- `identifier` ist der Name der Variable, mit dem diese verwendet werden kann
- `Datentyp` definiert, welche Art von Information in der Variable aufbewahrt werden kann

```kotlin
val identifier: Datentyp
```

## Initialization

Um eine Information in einer Variable zu speichern, muss die Variable zuerst deklariert werden.<br>
Nach der Deklaration, kann eine Variable initialisiert werden: d.h. in einer Variable wird zum ersten Mal ein Wert gespeichert.

 `=` ist der Zuweisungsoperator, mit dem einer Variable eine Information zugewiesen werden kann

```kotlin
val identifier: Datentyp = Information
```

## val vs var

    val = read-only variable -> d.h. nach dem Initialisieren kann keine weitere Zuweisung mehr stattfinden
    var = mutable variable   -> d.h. nach dem Initialisieren können beliebig viele Zuweisungen stattfinden

## Levels

Eine Variable kann an verschiedenen Stellen deklariert werden:

    - Top-Level variable = eine Variable, die direkt in einer .kt-Datei deklariert ist, ausserhalb von Klassen, Objekten oder Funktionen.
    - Property           = eine Variable, die innerhalb einer Klasse oder eines Objekts deklariert ist.
    - Local variable     = eine Variable, die innerhalb einer Funktion oder eines Codeblocks deklariert ist.

```kotlin
val topLevelVariable = "I am top-level"

fun main() {
    println(topLevelVariable)
    PropertyContainerClass().printProperty()
}

class PropertyContainerClass {
    
    private val myProperty = "I am a property"

    fun printProperty() {
        println(myProperty)

        val localVariable = "I am local"
        println(localVariable)
    }
}
```

## Type inference

Der Kotlin-Compiler kann bei einer Variablendeklaration mit direkter Zuweisung den Datentyp anhand des zugewiesenen Wertes erkennen.<br>
Dadurch kann in diesem Fall eine explizite Typ-Deklaration weggelassen werden:

```kotlin
val identifier = "auto-detect String as type because of type inference"
```

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Variables](https://kotlinlang.org/docs/basic-syntax.html#variables)
