# Variables

Eine Variable ist ein Container zum Speichern von Informationen. Sie

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
Nach der Deklaration, kann eine Variable initialisiert werden.<br>
Das heisst, in einer Variable wird zum ersten Mal einen Wert gespeichert.

- `=` ist der Zuweisungsoperator, mit dem in einer Variable eine Information gespeichert werden kann

```kotlin
val identifier: Datentyp = Information
```

## val vs var

    val = read-only variable -> d.h. nach dem Initialisieren kann keine weitere Zuweisung mehr stattfinden
    var = mutable variable   -> d.h. nach dem Initialisieren können beliebig viele Zuweisungen stattfinden

## Levels

Eine Variable kann an verschiedenen Stellen (Levels) deklariert werden:

    - Top-Level      = eine Variable ausserhalb von einer function
    - Local variable = eine Variable innerhalb einer function

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Variables](https://kotlinlang.org/docs/basic-syntax.html#variables)
