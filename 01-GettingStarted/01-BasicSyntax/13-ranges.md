##### 4/08/2020
# Basic Syntax - Ranges
Check if a number is within a range using `in` operator:

```kotlin
fun main() {
  val x = 10
  val y = 9

  if (x in 1..y + 1) {
    println("fits in range")
  }
}
```

Check if a number is out of range:

```kotlin
fun main() {
  val list = listOf("a", "b", "c")

  if (-1 !in 0..list.lastIndex) {
    println("-1 is out of range")
  }

  if (list.size !in list.indices) {
    println("list size is out of valid list indices range, too")
  }
}
```

Iterating over a range:

```kotlin
fun main() {
  for (x in 1..5) {
    print(x)
  }
}
```

Or over a progression:

```kotlin
fun main() {
  for (x in 1..10 step 2) {
    print(x)
  }

  println()

  for (x in 9 downTo 0 step 3) {
    print(x)
  }
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)