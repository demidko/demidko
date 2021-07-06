```kotlin
fun create(app: Idea) =
  when (app) {
    is Service -> use("github.com/demidko/service")
    is Utility -> use("github.com/demidko/utility") or("github.com/demidko/vcpkg-utility")
    is Android -> use("github.com/demidko/android")
    is Desktop -> use("github.com/demidko/desktop")
    is Library -> use("github.com/demidko/library")
    is Bot     -> use("github.com/demidko/telegram")
  }

```
### [`Login`](https://github.com/login) to use the new projects wizard buttons 
[![](https://img.shields.io/badge/service-EA7100?style=for-the-badge&logo=java)](https://github.com/demidko/service/generate) 
[![](https://img.shields.io/badge/utility(conan)-003E54?style=for-the-badge&logo=cmake)](https://github.com/demidko/conan-utility/generate) 
[![](https://img.shields.io/badge/utility(vcpkg)-003E54?style=for-the-badge&logo=cmake)](https://github.com/demidko/vcpkg-utility/generate) 
[![](https://img.shields.io/badge/android-darkgreen?style=for-the-badge&logo=android)](https://github.com/demidko/android/generate) 
[![](https://img.shields.io/badge/desktop-darkblue?style=for-the-badge&logo=kotlin)](https://github.com/demidko/desktop/generate)
[![](https://img.shields.io/badge/library-EA7100?style=for-the-badge&logo=java)](https://github.com/demidko/library/generate)
[![](https://img.shields.io/badge/telegram-blue?style=for-the-badge&logo=telegram)](https://github.com/demidko/telegram/generate) 
