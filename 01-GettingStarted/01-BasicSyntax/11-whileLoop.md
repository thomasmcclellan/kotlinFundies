##### 4/06/2020
# Basic Syntax - `while` Loop
```kotlin
fun main() {
  val items = listOf("apple", "banana", "kiwi")
  var index = 0

  while(index <items.size) {
    println("item at $index is ${items[index]}")
    index++
  }
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)