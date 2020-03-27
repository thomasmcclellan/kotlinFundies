##### 3/26/2020
# Basic Syntax - `Variables`
Read-only local `variables` are defined using the keyword `val`.  They can be assigned a value _only once_.

```kotlin
fun main() {
  val a: Int = 1 // immediate assignment
  val b = 2 // 'Int' type is inferred
  val c: Int // type required when no initializer is provided
  c = 3 // deferred assignment

  println("a = $a, b = $b, c = $c,")
}
```

`Variables` that can be reassigned use the `var` keyword:

```kotlin
fun main() {
  var x = 5 // 'Int' type is inferred
  x += 1 // able to be reassigned

  println("x = $x")
}
```

Top-level `variables`:

```kotlin
val PI = 3.14
var x = 0

fun incrementX() {
  x += 1
}

fun main() {
  println("x = $x; PI = $PI")

  incrementX()

  println("incrementX()")
  println("x = $x; PI = $PI")
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)