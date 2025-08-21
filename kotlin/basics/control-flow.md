# Control flow

1. Conditional expressions / statements
2. Ranges
3. Loops

## Conditional Expressions / Statements

### IF

- **if** prüft das Ergebnis eines einzigen booleschen Ausdrucks. Wenn das Ergebnis **true** ist, wird die angegebene Aktion ausgeführt<br>
- **if** hat einen optionalen **else**-branch, der ausgeführt wird, wenn das Ergebnis **false** ist<br>
- **if** kann beliebig verschachtelt/verkettet werden (nicht empfohlen, da schwer lesbar und daher fehleranfällig)<br>
- **if** kann sowohl als Anweisung (Statement) als auch als Ausdruck (Expression) verwendet werden<br>

### WHEN

- **when** prüft mehrere Ergebnisse von verschiedenen Bedingungen, die auf ein Subjekt angewendet werden<br>
- **when** verwendet `->`, um jede Bedingung von der Aktion zu trennen, die ausgeführt wird, wenn die entsprechende Bedingung **true** ist<br>
- **when** prüft alle Bedingungen sequentiell, bis eine Bedingung erfüllt ist.d.h. die erste Bedingung, die **true** ergibt, "gewinnt" (es gibt kein "Fall-Through")<br>
- **when** muss Bedingungen für alle möglichen Werte abdecken (es ist exhaustiv).d.h. dass normalerweise ein **else**-branch am Ende enthalten ist<br>
- **when** kann sowohl als Anweisung (Statement) als auch als Ausdruck (Expression) verwendet werden<br>
- **when** kann auch ohne ein Subjekt verwendet werden<br>

### Enpfehlung zur Anwendung
    
    für 1 Bedingung (simple boolean true false) use if
    für  n Bedingungen use when
    es gibt keinen condition ? then : else-Operator in Kotlin (wie in Java), aber da if ein Ausdruck ist geht folgendes: val result = if (condition) result1 else result2.

## Ranges

    1..4        -> um einen Wertebereich zu erstellen, der den Werten 1, 2, 3, 4 entspricht
    1..<4       -> um einen Wertebereich zu erstellen, der den Werten 1, 2, 3 entspricht
    4 downTo 1  -> um einen Wertebereich zu erstellen, der den Werten 4, 3, 2, 1 entspricht
    1..5 step 2 -> um einen Wertebereich zu erstellen, der den Werten 1, 3, 5 entspricht

* Ranges funktionieren auch mit Zeichen (Chars)!

## Loops

    for      -> iteriert über jedes Element in einer Collection, einem Bereich oder einem Array = behandelt alle Elemente         
    while    -> führt einen Codeblock aus, solange eine Bedingung true ist                      = könnte auch nie ausgeführt werden
    do-while -> führt den Codeblock zuerst aus und prüft danach die Bedingung                   = also mindestens 1 Ausführung

* **return** springt aus der nächstgelegenen umschliessenden Funktion zurück
* **break** beendet die nächstgelegene umschliessende Schleife.                                 
* **continue** springt zur nächsten Iteration der nächstgelegenen umschliessenden Schleife.                 

Kotlin Doku: [Control Flow](https://kotlinlang.org/docs/control-flow.html) oder direkt zur Kotlin Doku: [Control Flow](https://kotlinlang.org/docs/control-flow.html)
