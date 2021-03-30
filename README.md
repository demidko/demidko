```kotlin
fun create(app: Idea) = when (app) {
  is Service -> use("github.com/demidko/service")
  is Utility -> use("github.com/demidko/utility")
  is Android -> use("github.com/demidko/android")
  is Desktop -> use("github.com/demidko/desktop")
}
```
[![](https://img.shields.io/badge/kotlin-microservice-orange?style=for-the-badge&logo=kotlin)](https://github.com/demidko/service/generate) 
[![](https://img.shields.io/badge/c++23-utility-lightgray?style=for-the-badge&logo=cplusplus)](https://github.com/demidko/utility/generate) 
[![](https://img.shields.io/badge/kotlin-android%20app-green?style=for-the-badge&logo=android)](https://github.com/demidko/android/generate) 
[![](https://img.shields.io/badge/kotlin-desktop%20app-blue?style=for-the-badge&logo=kotlin)](https://github.com/demidko/desktop/generate)
