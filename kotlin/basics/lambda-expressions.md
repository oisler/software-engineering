# Lambda expressions

Lambda-Expressions sind `anonyme` Funktionen

    - Anonyme Funktion weil keine explizite Deklaration mit dem Keyword fun, einem identifier und einem Body in {} nötig ist
    - Stattdessen wird die Logik der Funktion direkt ausformuliert und als Wert behandelt
    - Eine Lambda expression entspricht im Wesentlichen dem Teil aus dem Body einer normalen Funktion

---

1. [Syntax](#syntax)
2. [Usage](#usage)
3. [it](#it)
5. [Higher order functions](#higher-order-functions)

---

## Syntax

Da Kotlin statisch typisiert ist, muss auch bei Lambdas ein Typ definiert sein, der beschreibt:
  - welche Parameter die Funktion akzeptiert (direkt vor dem `->`)
  - welchen Rückgabewert die Funktion liefert (nach dem `->`)

```kotlin
{ parameter: Typ -> Funktionskörper }
```

```kotlin
fun main() {
    // Explizite Typangabe
    val toUpperCaseExplizit: (String) -> String = { s -> s.uppercase() }
    println(toUpperCaseExplizit("i am learning kotlin"))

    // Implizite Typableitung
    val toUpperCase = { s: String -> s.uppercase() }
    println(toUpperCase("i am learning kotlin"))
}
```

## it

Wenn eine Lambda-Expression genau einen Parameter hat und der Typ aus dem Kontext abgeleitet werden kann, wird der Parameter automatisch mit dem Schlüsselwort it referenziert.
Die Typdeklaration kann in diesem Fall weggelassen werden.

```kotlin
val numbers = (0..10).toList()

// Implizit mit "it"
val even = numbers.filter { it % 2 == 0 }
println(even)

// Explizit mit Parameter und Typ
val odd = numbers.filter { number: Int -> number % 2 != 0 }
println(odd)
```

## Usage

Lambda-Expressions können:

1. als Inhalt einer Variable gespeichert werden
2. als Argument an eine andere Funktion übergeben werden
3. als Rückgabewert einer Funktion verwendet werden
4. direkt aufgerufen werden
 
## Higher order functions

Higher-Order Functions sind Funktionen, die:

    a) andere Funktionen als Parameter akzeptieren
    b) oder eine Funktion als Rückgabewert liefern.

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Lambda expressions](https://kotlinlang.org/docs/lambdas.html)
