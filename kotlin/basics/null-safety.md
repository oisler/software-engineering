# Null safety

`null` bedeutet auch in Kotlin nicht initialisiert (something is missing or not yet set) - Kotlin als Programmiersprache ist `null`-safe designed:

    - default mässig ist es nicht erlaubt, dass ein typ null ist (das wird zur compile-time geprüft)
    - es muss explizit deklariert werden, wenn ein typ null sein darf
  
---

1. [Nullable Types](#nullable-types)
2. [Check for null](#check-for-null)
3. [Safe call shortcut](#safe-call-shortcut)
4. [Elvis](#elvis-operator)

---

## Nullable types

Kotlin unterstützt Types die `null` sein können, das muss aber explizit deklariert werden

- `?` sorgt dafür, dass ein Typ, der eigentlich nicht `nullable` ist, trotzdem `nullable` sein darf

```kotlin
fun main() {
    var neverNull: String = "This can't be null"
    neverNull = null // Throws a compiler error

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

Damit nicht immer mit den üblichen `null`-checks gearbeitet werden muss, gibt es in Kotlin einen `null`-sicheren Operator als shortcut: 

- `?.` sorgt dafür, dass entweder der effektive Wert retourniert wird, oder `null` wenn das Objekt oder das Property halt `null` ist, oder ein call ganz geskipped wird (z.B. extension fun)
- `null`-sichere calls können aneinandergekettet werden

```kotlin
fun main() { 
    val nullString: String? = null
    println(nullString?.length)
    // null
}
```

## Elvis operator

Mithilfe vom Elvis-Operator können default values retourniert werden, wenn ein Wert `null` ist.

- `?:` retourniert den Wert auf der linken Seite, wenn er vorhanden ist und sonst den Wert auf der rechten Seite im `null`-case

```kotlin
fun main() {
    val nullString: String? = null
    println(nullString?.length ?: 0)
    // 0
}
```

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Null Safety](https://kotlinlang.org/docs/null-safety.html)
