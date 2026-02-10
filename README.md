# 📱 Modern Kotlin Chat App

Dự án ứng dụng Chat Real-time được xây dựng từ con số 0 nhằm mục đích rèn luyện kỹ năng lập trình Android hiện đại (Modern Android Development - MAD).

Ứng dụng sử dụng **Kotlin**, **Jetpack Compose** và **Clean Architecture**, kết nối với backend **Firebase** (tận dụng lại từ dự án Flutter cũ).

---

## 🛠 Công nghệ sử dụng (Tech Stack)

Dự án áp dụng các tiêu chuẩn và thư viện mới nhất của Google (2024-2025):

* **Ngôn ngữ:** [Kotlin](https://kotlinlang.org/) (100%)
* **Giao diện (UI):** [Jetpack Compose](https://developer.android.com/jetbrains/compose) (Material Design 3)
* **Kiến trúc:** Clean Architecture + MVI (Model-View-Intent)
* **Dependency Injection:** [Hilt](https://dagger.dev/hilt/)
* **Xử lý bất đồng bộ:** Coroutines & Flow
* **Điều hướng:** Navigation Compose (Type-Safe)
* **Backend:** Firebase (Authentication, Realtime Database/Firestore)
* **Build Tool:** Gradle KTS (Kotlin DSL) + Version Catalog

---

## 📂 Cấu trúc dự án (Clean Architecture)

Dự án được chia thành 3 tầng rõ ràng để đảm bảo tính độc lập và dễ bảo trì:

```text
com.example.chatappkotlin
├── data                 # Xử lý dữ liệu (Firebase, Room, API)
│   ├── model            # Data Models (DTO)
│   ├── repository       # Triển khai Repository
│   └── di               # Data Modules
├── domain               # Logic nghiệp vụ (Thuần Kotlin)
│   ├── model            # Domain Models
│   ├── repository       # Repository Interfaces
│   └── usecase          # Các Use Cases (VD: SendMessageUseCase)
├── presentation         # Giao diện người dùng
│   ├── theme            # Theme, Color, Type
│   ├── navigation       # App Navigation Graph
│   └── feature          # Các màn hình (Auth, Chat, Profile...)
└── di                   # Dependency Injection (App Module)
