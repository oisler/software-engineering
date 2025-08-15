# Control flow



1. Conditional expressions / statements
2. Ranges
3. Loops



### Conditional Expressions / Statements



* **if** checks a single boolean result of one conditional expression (may be comlex) within **()** and performs the declared action if the result is **true**
* **if** has an optional **else** branch, which is performed if the result is **false**
* **if** can be chained or nested as much as wanted but this is not recommended because it is not readable and leads to more mistakes



* **when** checks more than one result of multiple conditional expressions on a subject within **()**
* **when** uses **->** to separate each check from the action to take if the result of the corresponding conditional expression is true
* **when** checks all branch conditions sequentially until one of them is satisfied. This means: the first true condition wins (no fall-through)
* **when** must include conditions for all possible values (it is **exhaustive**); usually this leads to including an **else** condition and the end
* **when** can be used either as a **statement** or as an **expression**
* **when** can also be used without a subject



* for **1** condition (simple boolean true false) use **if**
* for **n** conditions use **when**
* **there** is no **condition ? then : else** construct in kotlin but if is an expression so it's like **val result = if (condition) result1 else result2**



### Ranges



* use **1..4** to create a range in Kotlin which is equivalent to 1, 2, 3, 4       **= regular**
* use **1..<4** to create a range in Kotlin which is equivalent to 1, 2, 3,        **= manipulate borders**
* use **4 downTo 1** to create a range in Kotlin which is equivalent to 4, 3, 2, 1 **= reverse order**
* use **1..5 step 2** to create a range in Kotlin which is equivalent to 1, 3, 5   **= manipulate increment**



* works also with Chars!

 

### Loops



* **for** simply iterates over every element in a collection, range or an Array        = all Elements         
* **while** executes a code block while a conditional expression is true               = may have 0 iterations
* **do-while** execute the code block first and then check the conditional expression  = at least 1 Iteration



* **return** by default returns from the nearest enclosing function or anonymous function
* **break** terminates he nearest enclosing loop                                         
* **continue** proceeds to the next step of the nearest enclosing loop                   



Kotlin Doku: [Control Flow](https://kotlinlang.org/docs/control-flow.html)

