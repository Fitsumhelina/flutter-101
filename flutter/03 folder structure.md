

## **1️⃣ Flutter Project Folder Structure (Typical)**

```
my_flutter_project/
│
├─ android/
│   ├─ app/
│   │   ├─ src/
│   │   │   ├─ main/
│   │   │   ├─ debug/
│   │   │   └─ profile/
│   │   └─ build.gradle.kts
│   ├─ build.gradle.kts
│   ├─ gradle/
│   ├─ gradle.properties
│   └─ settings.gradle.kts
│
├─ ios/
│   ├─ Flutter/
│   ├─ Runner/
│   ├─ Runner.xcodeproj/
│   ├─ Runner.xcworkspace/
│   └─ RunnerTests/
│
├─ lib/
│   └─ main.dart
│
├─ linux/
│   ├─ flutter/
│   ├─ runner/
│   └─ CMakeLists.txt
│
├─ macos/
│   └─ similar structure to iOS
│
├─ web/
│
├─ windows/
│
├─ test/
│
├─ .idea/
│   ├─ libraries/
│   ├─ runConfigurations/
│   ├─ modules.xml
│   └─ workspace.xml
│
├─ dart_tool/
│   ├─ dartpad/
│   ├─ extension_discovery/
│   ├─ flutter_build/
│   ├─ widget_preview_scaffold/
│   ├─ package_config.json
│   └─ package_graph.json
│
├─ build/
│
├─ metadata
├─ analysis_options.yaml
├─ pubspec.yaml
└─ pubspec.lock
```

---

## **2️⃣ Folder/File Purpose**

### **a) `dart_tool/`**

* **Purpose:** Internal folder used by **Dart and Flutter tools** for caching build outputs, packages, and tool-specific data.
* **Contents:**

  * `dartpad/` → Cache and data related to DartPad integration (web playground for Dart code).
  * `extension_discovery/` → Internal info for discovering Dart/Flutter extensions.
  * `flutter_build/` → Contains intermediate build artifacts for Flutter apps.
  * `widget_preview_scaffold/` → Used by Flutter dev tools for rendering widget previews.
  * `package_config.json` → Maps each package in the project to its location (used by the Dart analyzer and compiler).
  * `package_graph.json` → Dependency graph of all Dart packages in the project.

**💡 Note:** You usually **do not manually modify** anything in `dart_tool`. It’s auto-generated.

---

### **b) `.idea/`**

* **Purpose:** Stores **IntelliJ/Android Studio project settings**.
* **Contents:**

  * `libraries/` → Project library references.
  * `runConfigurations/` → Run/debug configurations for your project.
  * `modules.xml` → Modules included in the project.
  * `workspace.xml` → Personal workspace settings.

---

### **c) `android/`**

* **Purpose:** Android-specific build files.
* **Contents:**

  * `build.gradle.kts` (root) → Project-level Gradle build configuration.
  * `gradle.properties` → Gradle properties for configuration, performance tuning.
  * `settings.gradle.kts` → Which modules are included in the Gradle project.
  * `app/build.gradle.kts` → Module-level Gradle config (dependencies, compile SDK, flavors).
  * `app/src/main/` → Main app source code and resources.
  * `app/src/debug/` → Debug-specific configurations.
  * `app/src/profile/` → Profile-specific configurations.

---

### **d) `ios/`**

* **Purpose:** iOS-specific build files.
* **Contents:**

  * `Flutter/` → Generated Flutter framework for iOS.
  * `Runner/` → Xcode project files for the app.
  * `Runner.xcodeproj/` → Project settings.
  * `Runner.xcworkspace/` → Workspace settings for CocoaPods integration.
  * `RunnerTests/` → Unit/UI tests for iOS.

---

### **e) `lib/`**

* **Purpose:** Main **Dart code** lives here.
* `main.dart` → Entry point of the Flutter app.

---

### **f) `linux/`, `macos/`, `windows/`**

* Platform-specific desktop build folders.
* Typical content:

  * `runner/` → Platform runner code.
  * `CMakeLists.txt` → Build instructions for desktop apps.

---

### **g) `web/`**

* Holds web-specific build output and configuration (if building for web).

---

### **h) `test/`**

* Holds **unit and widget tests** for your Flutter app.

---

### **i) Root Project Files**

* `pubspec.yaml` → Project metadata, dependencies, and assets.
* `pubspec.lock` → Locked versions of dependencies.
* `analysis_options.yaml` → Dart/Flutter linter rules.
* `metadata` → Metadata about the project, e.g., Flutter version used.

---

### **💡 Smart Notes**

1. `dart_tool` + `.idea` are **auto-generated**; never manually modify unless you know what you’re doing.
2. `android/` and `ios/` are platform-specific bridges for Flutter.
3. `lib/` is the **heart of your app**; everything else is mostly support or configuration.
4. Build folders like `build/` and `dart_tool/flutter_build` **can be deleted safely**; Flutter will regenerate them.
5. Files like `package_config.json` ensure **IDE and compiler understand your dependencies correctly**.

