# Kotlin Value Classes

## Was?

Eine Value Class ist eine spezielle Klasse, die genau ein primäres Property hat.<br>
Sie wird verwendet, um semantisch klare Typen zu erstellen, ohne zusätzlichen Speicher-Overhead zu verursachen. 
Der Compiler entscheidet,<br>

a) ob die Value Class inline (d. h. nur der zugrunde liegende Wert wird verwendet)<br>
b) oder als normales Objekt (mit Speicher für eine Referenz)

dargestellt wird.

```kotlin
    @JvmInline
    value class User(val id: String)
```

## Warum?

1. Performance-Optimierung:<br>
Der Compiler entscheidet automatisch, ob die Value Class inline dargestellt werden kann, sodass nur der zugrunde liegende Wert verwendet wird.<br>
Daraus resultiert weniger Speicherverbrauch und weniger Garbage Collection.
      
2. Semantische Klarheit:<br>
Statt primitive Typen wie String oder Int direkt zu verwenden, können spezifische Typen definiert werden.
Das macht den Code verständlicher und sicherer.<br>
Ausserdem lassen sich spezifische Typen für when-Cases nutzen.
      
3. Typensicherheit:<br>
Value Classes verhindern, dass falsche Typen an Methoden übergeben werden.

## Wie?

1. Inline:
Die Value Class wird wie der zugrunde liegende Wert behandelt.<br>
Kein zusätzlicher Speicher-Overhead, da kein Objekt erstellt wird.<br>
Beispiele: Parameter, Rückgabewert, lokale Variable<br>
-> by value<br>       

2. Referenz:
Die Value Class wird wie ein normales Objekt behandelt.<br>
Speicher-Overhead durch Memory-Allokation für die Objektreferenz.<br>
Beispiele: Generics (z.B. List<T>), Nullable-Typen (?), Polymorphismus, Java-Interoperabilität<br>
-> by reference

## Wann?

Der Kotlin-Compiler entscheidet zur Compile-Time, ob eine Value Class inline dargestellt wird oder als normales Objekt. <br>
Diese Entscheidung basiert auf der Nutzung der Value Class (z. B. ob Referenzen benötigt werden).<br>
Das Verhalten ist fix und ändert sich nicht zur Runtime.<br>

## Spezialfall

Wenn das primary property einer value class nullable ist, kann es vom Comiler nicht als inline behandelt werden.
