##### 3/31/2020
# Basic Syntax - Conditional Expressions
```kotlin
fun maxOf(a: Int, b: Int) : Int {
  if (a > b) {
    return a
  } else {
    return b
  }
}

fun main() {
  println("max of 0 and 42 is ${maxOf(0, 42)})
}
```

In `Kotlin`, `if` can also be used as an expression:

```kotlin
fun maxOf(a: Int, b: Int) = if (a > b) a else b

fun main() {
  println("max of 0 and 42 is ${maxOf(0, 42)})
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)