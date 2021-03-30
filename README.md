```kotlin
fun create(app: Idea) = when (app) {
  is Service -> use("github.com/demidko/service")
  is Utility -> use("github.com/demidko/utility")
  is Android -> use("github.com/demidko/android")
  is Desktop -> use("github.com/demidko/desktop")
}
```
[![](https://img.shields.io/badge/kotlin-service-orange?style=for-the-badge&logo=appveyor)](https://github.com/demidko/service/generate)
[![](https://img.shields.io/badge/c++23-utility-blue)](https://github.com/demidko/utility/generate)
[![](https://img.shields.io/badge/kotlin-service-orange)](https://github.com/demidko/android/generate)
[![](https://img.shields.io/badge/kotlin-service-orange)](https://github.com/demidko/desktop/generate)
