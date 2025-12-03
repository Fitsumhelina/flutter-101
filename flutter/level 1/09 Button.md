

# 🎯 **NOTES – Buttons in Flutter**

Buttons are interactive widgets used to trigger actions (like submit, navigate, save, etc.)

Flutter provides **3 main modern buttons**:

1. **ElevatedButton**
2. **TextButton**
3. **OutlinedButton**

Plus some extra specialized buttons (IconButton, FloatingActionButton, etc.)

---

# 1️⃣ **ElevatedButton**

A button with background + shadow (raised effect).
Used when action is **important**.

### ✔ Example:

```dart
ElevatedButton(
  onPressed: () {
    print("Button Pressed!");
  },
  child: Text("Click Me"),
)
```

### 📌 Common Properties

* `onPressed` → action when clicked
* `child` → text/icon
* `style` → customize look

---

# 2️⃣ **TextButton**

Flat button with only text.
Used for low-priority actions like “Cancel”, “Skip”.

### ✔ Example:

```dart
TextButton(
  onPressed: () {},
  child: Text("Skip"),
)
```

---

# 3️⃣ **OutlinedButton**

Button with only an outline (border).
Looks modern + less heavy.

### ✔ Example:

```dart
OutlinedButton(
  onPressed: () {},
  child: Text("Register"),
)
```

---

# 🎨 Styling Buttons (Very Important)

### ✔ Common styling method:

```dart
ElevatedButton(
  style: ElevatedButton.styleFrom(
    backgroundColor: Colors.blue,
    foregroundColor: Colors.white,
    padding: EdgeInsets.symmetric(vertical: 12, horizontal: 20),
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(10),
    ),
  ),
  onPressed: () {},
  child: Text("Login"),
)
```

---

# ✴️ Icon Button

Used when you want **only an icon**.

```dart
IconButton(
  icon: Icon(Icons.home),
  onPressed: () {},
)
```

---

# 🌕 FloatingActionButton (FAB)

Circular button used for main action on a screen
(example: add new item)

```dart
FloatingActionButton(
  onPressed: () {},
  child: Icon(Icons.add),
)
```

---

# 🔥 Buttons with Icons

### Elevated Button with Icon

```dart
ElevatedButton.icon(
  onPressed: () {},
  icon: Icon(Icons.send),
  label: Text("Send"),
)
```

---

# 📚 Full Comparison Table

| Button Type              | Look            | Use Case                |
| ------------------------ | --------------- | ----------------------- |
| **ElevatedButton**       | Filled + shadow | Important action        |
| **TextButton**           | Text only       | Less important / footer |
| **OutlinedButton**       | Border only     | Medium importance       |
| **IconButton**           | Icon only       | Toolbar / small actions |
| **FloatingActionButton** | Round           | Primary screen action   |

---

# 🧠 Quick Memory Trick

| Need                       | Button             |
| -------------------------- | ------------------ |
| Big action                 | **ElevatedButton** |
| Soft action                | **TextButton**     |
| Border-style modern action | **OutlinedButton** |
| Icon only                  | **IconButton**     |
| Main screen action         | **FAB**            |

---

