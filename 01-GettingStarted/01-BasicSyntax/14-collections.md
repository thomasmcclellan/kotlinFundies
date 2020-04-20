##### 4/09/2020
# Basic Syntax - Collections
Iterating over a collection:

```kotlin
fun main() {
  val items = listOf("apples", "banana", "kiwi")

  for (item in items) {
    println(item)
  }
}
```

Checking if a collection contains an `object` using `in` operator:

```kotlin
fun main() {
  val items = setOf("apple", "banana", "kiwi")

  when {
    "orange" in items -> println("juicy")
    "apple" in items -> println("apple is fine too")
  }
}
```

Using `lambda` expressions to filter and map collections:

```kotlin
fun main() {
  val fruits = listOf("banana", "avocado", "apple", "kiwi")

  fruits
    .filter { it.startsWith("a") }
    .sortedBy { it }
    .map { it.toUpperCase() }
    .forEach { println(it) }
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)