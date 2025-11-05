# Null safety

`null` bedeutet auch in Kotlin nicht initialisiert (something is missing or not yet set) und Kotlin als Programmiersprache ist `null`-safe designed:

    - default mässig ist es nicht erlaubt, dass ein typ null ist
    - es muss explizit deklariert werden, wenn ein typ null sein darf
  
---

1. [Nullable Types](#nullable-types)
2. [Check for null](#check-for-null)
3. [Safe call shortcut](#safe-call-shortcut)
---

## Nullable types

Kotlin unterstützt Types die `null` sein können:

- `?` sorgt dafür, dass ein Typ, der nicht  `null` sein darf,  `nullable` wird

```kotlin
fun main() {
    // neverNull has String type
    var neverNull: String = "This can't be null"

    // Throws a compiler error
    neverNull = null

    // nullable has nullable String type
    var nullable: String? = null
    nullable = "You can keep a null here"
}
```

## Check for null

In Kotlin werden `null`-checks mit conditional expressions durchgeführt:

```kotlin
fun main() {
    var nullable: String? = null

     if (nullable == null) {
         nullable = "You can keep a null here" 
     }

      if (nullable != null) {
         println(nullable.length)
     }     
}
```

## Safe call shortcut

Damit nicht immer mit den üblichen `null`-checks gearbeitet werden muss, gibt es in Kotlin einen `null`-sicheren Operator: 

- `?.` sorgt dafür, dass entweder der effektive Wert retourniert wird, oder `null` wenn das Objekt oder das Property halt `null` ist, oder ein call ganz geskipped wird (z.B. extension fun)
- `null`-sichere calls können aneinandergekettet werden

```kotlin
fun lengthString(maybeString: String?): Int? = maybeString?.length

fun main() { 
    val nullString: String? = null
    println(lengthString(nullString))
    // null
}
```

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Null Safety](https://kotlinlang.org/docs/null-safety.html)
