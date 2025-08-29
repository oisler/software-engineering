# Lambda expressions

Lambda-Expressions sind `anonyme` Funktionen

    - Anonyme Funktion weil keine explizite Deklaration mit dem Keyword fun, einem identifier und einem Body in {} nötig ist
    - Stattdessen wird die Logik der Funktion direkt ausformuliert und als Wert behandelt
    - Eine Lambda expression entspricht im Wesentlichen dem Teil aus dem Body einer normalen Funktion

---

1. [Syntax](#syntax)
2. [Usage](#usage)
3. [it](#it)
4. [Implizit Explizit Return](#implizit-explizit-return)
5. [Higher order functions](#higher-order-functions)

---

## Syntax

Da Kotlin statisch typisiert ist, muss auch bei Lambdas ein Typ definiert sein, der beschreibt:
  - welche Parameter die Funktion akzeptiert und zwar kommasepariert in ()
  - welchen Rückgabewert die Funktion liefert und zwar nach dem `->`

```kotlin
{ parameter: Typ -> Statement }
```

```kotlin
fun main() {
    val toUpperCaseExplizit: (String) -> String = { s -> s.uppercase() }
    println(toUpperCaseExplizit("i am learning kotlin"))
}
```

```kotlin
fun main() {
    val toUpperCase = { s: String -> s.uppercase() }
    println(toUpperCase("i am learning kotlin"))
}
```

## it

Häufig haben Lambda Expressions genau einen Parameter.<br>
Wenn der Compiler alle notwendigen Infos aus dem Kontext ableiten kann, darf die Typ deklaration weggelassen werden:

```kotlin
fun main() {
    val numbers = (0..10).toList()
    val even = numbers.filter { it % 2 == 0 } // implizit mit it
    println(even)
}
```

```kotlin
fun main() {
    val numbers = (0..10).toList()
    val odd = numbers.filter { number: Int -> number % 2 != 0 } // explizit mit identifier und Typ
    println(odd)
}
```

## Usage

Lambda expressions können
1. als Inhalt einer Variable gespeichert werden
2. als Argument an eine andere Funktion übergeben werden
3. als Resultat einer aufgerufenen Funktion retourniert werden
4. direkt aufgerufen werden

 
## Higher order functions

Higher-Order Functions sind Funktionen, die:

    a) andere Funktionen als Parameter akzeptieren
    b) oder eine Funktion als Rückgabewert liefern.

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Lambda expressions](https://kotlinlang.org/docs/lambdas.html)
