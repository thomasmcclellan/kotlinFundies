##### 4/01/2020
# Basic Syntax - Nullable Values and `null` Checks
A reference must be explicitly marked as nullable when `null` value is possible.

Return `null` if `str` does not hold an integer:

```kotlin
fun parseInt(str: String) : Int? {
  // ...
}
```

Use a `function` returning nullable value:

```kotlin
fun parseInt(str: String) : Int? {
  return str.toItOrNull()
}

fun printProduct(arg1: String, arg2: String) {
  val x = parseInt(arg1)
  val y = parseInt(arg2)

  // Using 'x * y' yields error because they may hold nulls
  if (x != null && y != null) {
    // x and y are automatically cast to non-nullable after null checks
    println(x * y)
  }
  else {
    println("'$arg1' or '$arg2' is not a number")
  }
}

fun main() {
  printProduct("6", "7")
  printProduct("a", "7")
  printProduct("a", "b")
}
```

or

```kotlin
fun parseInt(str: String) : Int? {
  return str.toItOrNull()
}

fun printProduct(arg1: String, arg2: String) {
  val x = parseInt(arg1)
  val y = parseInt(arg2)

  // ...
  if (x == null) {
    println("Wrong number format in arg1: '$arg1'")
  }
  if (y === null) {
    println("Wrong number format in arg2: '$arg2'")
  }

  // x and y are automatically cast to non-nullable after null check
  println(x * y)
}

fun main() {
  printProduct("6", "7")
  printProduct("a", "7")
  printProduct("99", "b")
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)