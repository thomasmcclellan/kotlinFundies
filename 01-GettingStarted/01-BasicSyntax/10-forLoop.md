##### 4/03/2020
# Basic Syntax - `for` Loop
```kotlin
fun main() {
  val items = listOf("apple", "banana", "kiwi")

  for (item in items) {
    println(item)
  }
}
```

or 

```kotlin
fun main() {
  val items = listOf("apple", "banana", "kiwi")

  for (index in items.indices) {
    println("Item at $index is ${items[index]}")
  }
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)