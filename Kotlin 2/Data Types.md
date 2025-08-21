# Data Types

Every variable and data structure in Kotlin has a type.
Types tell the compiler what you are allowed to do with that variable or data structure.
In Kotlin, everything is an object in the sense that you can call member functions and properties on any variable.
Kotlin's ability to infer the type is called type inference.

### Basic Types

The Basic types have an optimized internal representation as primitive values at runtime.

Category               | Basic Types
-----------------------|----------------------------
Integers               | Byte, Short, Int, Long
Unsigned integers      | UByte, UShort, UInt, ULong
Floating-point numbers | Float, Double
Booleans               | Boolean
Characters             | Char
Strings                | Strings
Data Structure         | Arrays

The difference between an integer and an unsigned integer is:

* integer          → min value is negative                                                  → Byte goes from -128 to 127
* unsigned integer → min value is zero, use the full bit range to represent positive values → UByte goes from 0 to 255

#### Other Types

* Any
* Nothing
* Unit

#### Type checks and casts

* checks = check the type of an object at runtime
* cast   = convert objects to a different type at runtime



Kotlin Doku: [Types](https://kotlinlang.org/docs/basic-types.html)

🔙 [Back to Kotlin Overview](kotlin/README.md)
