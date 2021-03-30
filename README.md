```kotlin
fun create(app: Idea){
  login("github.com")
  when (app) {
    is Service -> use("github.com/demidko/service")
    is Utility -> use("github.com/demidko/utility")
    is Android -> use("github.com/demidko/android")
    is Desktop -> use("github.com/demidko/desktop")
  }
}
```
[![](https://img.shields.io/badge/microservice-orange?style=for-the-badge&logo=kotlin)](https://github.com/demidko/service/generate) 
[![](https://img.shields.io/badge/c++23-utility-gray?style=for-the-badge&logo=cplusplus)](https://github.com/demidko/utility/generate) 
[![](https://img.shields.io/badge/android-darkgreen?style=for-the-badge&logo=android)](https://github.com/demidko/android/generate) 
[![](https://img.shields.io/badge/desktop-darkblue?style=for-the-badge&logo=kotlin)](https://github.com/demidko/desktop/generate)
