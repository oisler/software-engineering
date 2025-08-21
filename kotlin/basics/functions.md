# Functions

1. [Allgemein](#allgemein)
2. [Basic Declaration](#basic-declaration)
3. [Named arguments und Default values](#named-arguments-und-default-values)
4. [Without return und Early Return](#without-return-und-early-return)
5. [Single-expression functions](#single-expression-functions)

## Allgemein

Eine Funktion

    - beinhaltet die Anweisungen zur Lösung einer bestimmten Aufgabe
    - wird einmal deklariert und kann anschliessend beliebig oft verwendet werden
    - kann ein Ergebnis liefern oder auch nicht

## Basic Declaration

Um eine Funktion zu deklarieren, braucht es verschiedene Informationen:

- `fun` ist das Keyword, um die Deklaration einer function einzuleiten
- `identifier` ist der Name der function, mit dem diese verwendet werden kann
- `()` beinhalten Parameter mit einem konkreten Datentyp, um Argumente von ausserhalb in eine Funktion zu übergeben
- `ReturnType` ist der Datentyp des Ergebnis, falls die Funktion ein Ergebnis produziert
- `{}` beinhalten die einzelnen Anweisungen, die die Funktion ausführen soll

```kotlin
fun identifier(p1: Datentyp): ReturnType {
    // do something cool
}
```

## Named arguments und Default values

- **Named arguments**: beim Funktionsaufruf wird explizit angeben, welches Argument zu welchem Parameter gehört
- **Default values**: ein Argument muss für diesen Parameter nicht angegeben werden, da der Standardwert verwendet wird

```kotlin
fun mergeStrings(p1: String, p2: String, p3: String = "very "): String {
    return "Kotlin is $p3$p1$p2"
}

fun main() {
    val result = mergeStrings("cool", "🙂")  // ohne Named arguments aber default verwenden
    println(result)
    
    val result2 = mergeStrings(p1 = "cool", p2 = "🙂")  // mit Named arguments und default
    println(result2)
    
    val result3 = mergeStrings(p2 = "🙂", p1 = "cool") // mit Named arguments und default in anderer Reihenfolge
    println(result3)
    
    val result4 = mergeStrings(p3 = "heavy ", p2 = "🙂", p1 = "cool") // mit Named arguments ohne default und in anderer Reihenfolge
    println(result4)
}
```

- **Named arguments** machen Funktionsaufrufe lesbarer und ermöglichen es, Argumente in beliebiger Reihenfolge anzugeben
- **Default values** erlauben es, Argumente wegzulassen und definierte Standardwerte zu verwenden
- Die Kombination aus beiden Konzepten macht Funktionen noch flexibler und einfacher zu verwenden
- Wird ein Parameter geskipped, müssen alle anderen benannt werden

## Without return und Early Return

Funktionen in Kotlin können Ergebnisse liefern oder auch nicht.<br>
Funktionen mit Ergebnis müssen mindestens ein `return`-Statement enthalten<br>
Funktionen ohne Ergebnis brauchen nicht zwingend ein `return`-Statement<br>
In Funktionen ohne Ergebnis, kann das `return`-Statement verwendet werden, um die Verarbeitung vorzeitig abzubrechen<br>

```kotlin
fun withReturn(): String {
    return "My return value is a String"
}

fun withoutReturn(): Unit {
    println("I have no return value")
}

fun earlyReturn(s: String): Unit {
    if (s != "print me") return
    println(s)
}

fun main() {
    println(withReturn())
    withoutReturn()
    
    earlyReturn("hit early return")
    earlyReturn("print me")
}
```

## Single-expression functions

In Kotlin können Funktionen, die nur einen einzigen Ausdruck enthalten, als Single-Expression-Funktionen geschrieben werden.<br>
D.h. der Body in geschweiften Klammern `{}` kann weggelassen werden.<br>
Stattdessen wird der Ausdruck direkt nach dem Gleichheitszeichen `=` angegeben.<br>
Single-Expression-Funktionen sind besonders nützlich für kurze, einfache Berechnungen oder Getter-Funktionen.<br>
Der Rückgabetyp kann weggelassen werden, wenn der Compiler ihn durch Type Inference ableiten kann.<br>

Vorteile:
1. Kürzerer Code
2. Bessere Lesbarkeit, weil der Fokus auf dem Ausdruck liegt

```kotlin
fun main() {
    val firstNumber = 2
    val secondNumber = 21
    
    multiply(firstNumber, secondNumber)
    multiplySingleExpression(firstNumber, secondNumber)
}

fun multiply(first: Int, second: Int) {
    println(first * second)
}

fun multiplySingleExpression(first: Int, second: Int) = println(first * second)
```

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Functions](https://kotlinlang.org/docs/functions.html)
