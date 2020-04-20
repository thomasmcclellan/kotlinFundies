##### 4/07/2020
# Basic Syntax - `when` Expression
```kotlin
fun describe(obj: Any) : String = 
  when(obj) {
    1         -> "One"
    "Hello"   -> "Greeting"
    is Long   -> "Long"
    !is Long  -> "Not a string"
    else      -> "Unknown"
  }

fun main() {
  println(describe(1))
  println(describe("Hello"))
  println(describe(1000L))
  println(describe(2))
  println(describe("other"))
}
```

---

[Kotlin Docs](https://kotlinlang.org/docs/reference/basic-syntax.html)