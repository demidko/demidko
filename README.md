```kotlin
fun create(application: Idea) = when (application) {
  is Utility -> use("")
  is DesktopUI -> use("")
  is Microservice -> use("")
  is AndroidApplication -> use("")
}
```
