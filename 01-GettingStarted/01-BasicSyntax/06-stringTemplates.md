##### 3/30/2020
# Basic Syntax - `String` Templates
```kotlin
fun main() {
  var a = 1
  val s1 = "a is $a"

  a = 2
  val s2 = "${s1.replace("is", "was")}, but now is $a"

  println(s2)
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)