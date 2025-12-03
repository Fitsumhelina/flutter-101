# 📘 **Notes: pub.dev, Hive & hive_flutter (1.1.0)**

## **1. What is pub.dev?**

* **pub.dev** is Flutter’s official package repository.
* Used to search, find, and install packages for:

  * State management
  * Databases
  * UI widgets
  * APIs
  * Utilities
* It provides:

  * Package version info
  * Installation instructions
  * Null-safety support
  * Example code & documentation

---

# 🐝 **2. What is Hive?**

* **Hive is a lightweight, NoSQL database** written in pure Dart.
* Works fast on Android, iOS, Web, and Desktop.
* Key features:

  * Very fast read/write
  * Offline storage
  * Strongly typed data
  * Requires no native dependencies
  * Good for small datasets

### **Use Cases**

* Storing user settings
* Caching API data
* Storing simple app data locally

---

# 📱 **3. hive_flutter**

* A Flutter extension for Hive.
* Supports:

  * `Hive.initFlutter()` → Initializes Hive in Flutter
  * Works with application directories automatically

### **Version used**

* **hive_flutter 1.1.0**

---

# 🧩 **4. Add these to pubspec.yaml**

Here is the **correct way** to add Hive and hive_flutter under dependencies:

```yaml
dependencies:
  flutter:
    sdk: flutter

  hive: ^2.0.5
  hive_flutter: ^1.1.0
```

✔ Use `^` to allow minor updates
✔ Ensure proper indentation
✔ Always place 2 spaces before keys under dependencies

---

# 📦 **5. After adding dependencies**

Run:

```bash
flutter pub get
```

---

# 🏗 **6. Initialize Hive in main.dart**

```dart
void main() async {
  WidgetsFlutterBinding.ensureInitialized();

  await Hive.initFlutter();  // important

  runApp(MyApp());
}
```

---

# 🗃 **7. Opening a Box**

```dart
var box = await Hive.openBox('myBox');

box.put('name', 'John');
print(box.get('name'));
```

---
