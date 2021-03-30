```kotlin
fun create(app: Idea) = when (app) {
  is Utility -> use("")
  is DesktopUI -> use("")
  is Microservice -> use("")
  is AndroidApplication -> use("")
}
```
