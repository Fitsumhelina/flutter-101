

# 🧱 **What Is a StatelessWidget?**

A **StatelessWidget** is a widget that:

* **Does not store any state internally**
* **Cannot change over time**
* **Always builds the same UI for the same input**
* Is ideal for **static UI components**

If something needs to update while the app is running (text change, color change, toggle, animation), then it **should NOT** be a StatelessWidget — it should be a **StatefulWidget**.

---

# 🧠 **When to Use StatelessWidget**

Use a StatelessWidget if:

* The UI is constant.
* All data needed to build the UI is passed from outside (via constructor).
* The widget does NOT need to update itself during runtime.

### Examples:

✔ Buttons
✔ Icons
✔ Text widgets
✔ Custom UI components that receive fixed data
✔ Navigation pages that do not change internally

---

# 📝 **Simple Example**

```dart
import 'package:flutter/material.dart';

class MyStatelessWidget extends StatelessWidget {
  final String title;

  MyStatelessWidget({required this.title});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text(title)),
      body: Center(child: Text("This is a Stateless Widget")),
    );
  }
}
```

### ✔ What is happening?

* `title` is passed through the constructor.
* The widget uses that value to build the UI.
* UI will not change unless a parent widget rebuilds it.

---

# 🧩 **Key Characteristics**

### 1️⃣ **Immutable**

The widget cannot change its values after creation.

```dart
final String name; // final is required
```

### 2️⃣ **No setState()**

StatelessWidget does NOT have access to `setState()`.

### 3️⃣ **Rebuild occurs only when parent rebuilds**

Flutter rebuilds a StatelessWidget when the parent widget rebuilds or when dependencies change.

---

# 🏗 How StatelessWidget Works (Internally)

1. Constructor gets called
2. Flutter calls `build()`
3. The widget displays UI
4. The widget **never changes by itself**

If something changes, Flutter destroys the old widget and creates a **new instance** of it.

---

# 🆚 StatelessWidget vs StatefulWidget

| Feature             | StatelessWidget | StatefulWidget      |
| ------------------- | --------------- | ------------------- |
| Can update UI?      | ❌ No            | ✔ Yes               |
| Has internal state? | ❌ No            | ✔ Yes               |
| Has setState()?     | ❌ No            | ✔ Yes               |
| Best for            | Static UI       | Dynamic/changing UI |
| Memory              | Lightweight     | Slightly heavier    |

---

# 🎯 Summary (Smart Note)

* **StatelessWidget = no internal changes, UI stays same.**
* Use it for **static screens, icons, labels, layout widgets**.
* If UI updates during runtime → use **StatefulWidget** instead.
* StatelessWidget rebuilds only when the **parent** rebuilds.

