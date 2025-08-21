# Data Types

Ein Datentyp definiert welche Art von Information in einer Variable oder einer Datenstruktur gespeichert werden kann.<br>

    In Kotlin hat jede Variable und jede Datenstruktur einen expliziten Datentyp
    In Kotlin ist alles ein Objekt, im Sinne davon, dass auf jeder Variable Funktionen und Eigenschaften aufgerufen werden können

---

1. [Basic Types](#basic-types)
2. [Other Types](#other-types)
3. [Type checks and casts](#type-checks-and-casts)

---

## Basic Types

Kotlin kennt folgende basic types:

| Category                 | Basic Types                    |
|--------------------------|--------------------------------|
| Integers                 | Byte, Short, Int, Long         |
| Unsigned integers        | UByte, UShort, UInt, ULong     |
| Floating-point numbers   | Float, Double                  |
| Booleans                 | Boolean                        |
| Characters               | Char                           |
| Strings                  | String                         |

Der Unterschied zwischen einem integer und einem unsigned integer ist:

    integer          → min value ist negativ                                                                           → ex Byte: -128 to 127
    unsigned integer → min value ist zero, so dass der gesamte Bitbereich genutzt wird, um positive Werte darzustellen → ex UByte:   0 to 255

## Other Types

* Any
* Nothing
* Unit
  
## Type checks and casts

* checks = check the type of an object at runtime
* cast   = convert objects to a different type at runtime

🔙 [Back to Kotlin Overview](../README.md) oder direkt zur Kotlin Doku: [Types](https://kotlinlang.org/docs/basic-types.html)
