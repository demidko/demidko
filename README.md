```kotlin
fun create(app: Idea) {
  when (app) {
    is Service -> use("github.com/demidko/service/generate")
    is Utility -> use("github.com/demidko/utility/generate")
    is Android -> use("github.com/demidko/android/generate")
    is Desktop -> use("github.com/demidko/desktop/generate")
  }
}
```
## [`Login`](https://github.com/login) and select your project type
[![](https://img.shields.io/badge/microservice-EA7100?style=for-the-badge&logo=java)](https://github.com/demidko/service/generate) 
[![](https://img.shields.io/badge/utility-003E54?style=for-the-badge&logo=cmake)](https://github.com/demidko/utility/generate) 
[![](https://img.shields.io/badge/android%20app-darkgreen?style=for-the-badge&logo=android)](https://github.com/demidko/android/generate) 
[![](https://img.shields.io/badge/desktop%20gui-darkblue?style=for-the-badge&logo=kotlin)](https://github.com/demidko/desktop/generate)
