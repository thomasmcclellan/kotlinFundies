##### 3/25/2020
# Basic Syntax - `Functions`
`Function` having two `Int` parameters with `Int` return type:

```kotlin
fun sum(a: Int, b: Int) : Int {
  return a + b
}

fun main() {
  print("sum of 3 and 5 is ")
  println(sum(3, 5))
}
```

`Function` with an expression body and inferred return type:

```kotlin
fun sum(a: Int, b: Int) = a + b

fun main() {
  println("sum of 19 and 23 is ${sum(19, 23)}")
}
```

`Function` returning no meaningful value:

```kotlin
fun printSum(a: Int, b: Int) : Unit {
  println("sum of $a and $b is ${a + b}")
}

fun main() {
  printSum(-1, 8)
}
```

`Unit` return type can be omitted:

```kotlin
fun printSum(a: Int, b: Int) {
  println("sum of $a and $b is ${a + b}")
}

fun main() {
  printSum(-1, 8)
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)