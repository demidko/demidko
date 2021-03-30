```kotlin
fun create(app: Idea) = when (app) {
  is Service -> use(" https://github.com/demidko/service ")
  is Utility -> use(" https://github.com/demidko/utility ")
  is Android -> use(" https://github.com/demidko/android ")
  is Desktop -> use(" https://github.com/demidko/desktop ")
}
```
