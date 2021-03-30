### [`Login to use project wizard magic buttons`](https://github.com/login)
```kotlin
fun create(app: Idea) {
  when (app) {
    is Service -> use("github.com/demidko/service)
    is Utility -> use("github.com/demidko/utility")
    is Android -> use("github.com/demidko/android")
    is Desktop -> use("github.com/demidko/desktop")
  }
}
```
[![](https://img.shields.io/badge/microservice-EA7100?style=for-the-badge&logo=kotlin)](https://github.com/demidko/service/generate) 
[![](https://img.shields.io/badge/utility-003E54?style=for-the-badge&logo=cmake)](https://github.com/demidko/utility/generate) 
[![](https://img.shields.io/badge/android-darkgreen?style=for-the-badge&logo=android)](https://github.com/demidko/android/generate) 
[![](https://img.shields.io/badge/desktop-darkblue?style=for-the-badge&logo=kotlin)](https://github.com/demidko/desktop/generate)
