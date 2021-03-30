```kotlin
fun create(app: Idea) = when (app) {
  is Service -> use("github.com/demidko/service")
  is Utility -> use("github.com/demidko/utility")
  is Android -> use("github.com/demidko/android")
  is Desktop -> use("github.com/demidko/desktop")
}
```
[![service](https://img.shields.io/badge/kotlin-service-orange)](https://confluence.jetbrains.com/display/ALL/JetBrains+on+GitHub)
