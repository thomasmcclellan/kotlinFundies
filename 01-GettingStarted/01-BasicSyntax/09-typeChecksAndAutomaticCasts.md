##### 4/02/2020
# Basic Syntax - Type Checks and Automatic Casts
The `is` operator checks if an expression is an instance of a type.  If an immutable local variable or property is checked for a specific type, there's no need to cast it explicitly:

```kotlin
fun getStringLength(obj: Any) : Int? {
  if (obj is String) {
    // 'obj' is automatically cast to 'String' in this branch
    return obj.length
  }

  // 'obj' is still of type 'Any' outside of the type-checked branch
  return null
}

fun main() {
  fun printLength(obj: Any) {
    println("'$obj' string length is ${getStringLength(obj) ? "... err, not a string"} ")
  }

  printLength("Incomprehensibilities")
  printLength(1000)
  printLength(listOf(Any()))
}
```

or

```kotlin
fun getStringLength(obj: Any) : Int? {
  if (obj !is String) return null

  // 'obj' is automatically cast to 'String' in this branch
  return obj.length
}

fun main() {
  fun printLength(obj: Any) {
    println("'$obj' string length is ${getStringLength(obj) ? "... err, not a string"} ")
  }

  printLength("Incomprehensibilities")
  printLength(1000)
  printLength(listOf(Any()))
}
```

or even

```kotlin
fun getStringLength(obj: Any) : Int? {
  // 'obj' is automatically cast to 'String' to the right-hand side of '&&'
  if (obj is String && obj.length > 0) return obj.length

  return null
}

fun main() {
  fun printLength(obj: Any) {
    println("'$obj' string length is ${getStringLength(obj) ? "... err, not a string"} ")
  }

  printLength("Incomprehensibilities")
  printLength(1000)
  printLength(listOf(Any()))
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)