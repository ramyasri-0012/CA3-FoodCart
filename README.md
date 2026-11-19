# CA3 FoodCart - Android Application 🛒

An Android Shopping Cart application built with **Jetpack Compose**, **Material 3**, and **Room Database**. The app allows users to manage their shopping cart items with full CRUD (Create, Read, Update, Delete) operations and persistent local storage.

---

## 🌟 Features

- **Product Input Form**: Add items with Product Name, Price (₹), and Quantity.
- **Smart Item Aggregation**: Automatically updates quantities for existing items instead of creating duplicates.
- **Quantity Constraints**: Enforces a minimum quantity of `1` for all cart items.
- **Room Database Integration**: Offline persistent storage using Room ORM with Kotlin Flow & StateFlow.
- **Dynamic Item Cards**: Each card displays a product emoji thumbnail, name, quantity, price breakdown (`₹Price x Qty = Total`), and action buttons.
- **Update & Delete Actions**: Interactively edit product details via an update dialog or remove items from the cart.
- **Empty State UI**: Clean, friendly UI placeholder displayed when the cart is empty.

---

## 🛠️ Tech Stack & Architecture

- **Language**: Kotlin 2.2.10
- **UI Framework**: Jetpack Compose with Material 3
- **Database**: Room Database 2.8.5 with KSP (Kotlin Symbol Processing)
- **Architecture**: MVVM (Model-View-ViewModel)
- **Asynchronous Work**: Kotlin Coroutines, StateFlow, Flow
- **Minimum SDK**: API 24 (Android 7.0)
- **Target SDK**: API 37 (Android 15)

---

## 📁 Project Structure

```text
app/src/main/java/
└── MainActivity.kt       # Contains Room Entity, DAO, Database, ViewModel & Compose UI
```

### Key Components

1. **`CartItem`**: Room Entity representing a cart item (`id`, `name`, `price`, `quantity`).
2. **`CartDao`**: Data Access Object defining queries for Insert, Update, Delete, and Flow observation.
3. **`CartDatabase`**: Room Database instance provider.
4. **`CartViewModel`**: ViewModel managing state and business logic using `StateFlow`.
5. **`MyCartApp`**: Top-level Composable screen rendering the top bar, form, empty view, and item list.

---

## 🚀 How to Run

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ramyasri-0012/CA3-FoodCart.git
   ```
2. **Open in Android Studio**:
   - Select **Open an existing project** and choose the `CA3-FoodCart` folder.
3. **Sync Gradle**:
   - Wait for Android Studio to finish syncing Gradle dependencies.
4. **Run the App**:
   - Connect an Android device or start an emulator.
   - Click **Run ▶️** or press `Shift + F10`.

---

## 📜 License

Distributed under the MIT License.
