# 🚀 **NOTE – FloatingActionButton (FAB)**

---

# 🎯 **1. What is a Floating Action Button?**

A **FloatingActionButton (FAB)** is a **circular button** that floats above the UI — usually on the **bottom-right corner**.

It is used for the **primary action** of the screen.

Examples:

* 📩 Add message
* ➕ Add item
* ✏️ Edit
* 🔍 Search
* 📷 Camera

---

# ⭐ **2. Basic FAB Example**

```dart
FloatingActionButton(
  onPressed: () {
    print("Button Pressed");
  },
  child: Icon(Icons.add),
)
```

✔ `onPressed` → required
✔ `child` → usually an Icon

---

# 🔵 **3. FAB With Scaffold**

Usually placed inside the Scaffold:

```dart
Scaffold(
  appBar: AppBar(title: Text("FAB Example")),
  floatingActionButton: FloatingActionButton(
    child: Icon(Icons.add),
    onPressed: () {},
  ),
)
```

---

# 🎨 **4. Important Properties (SMART SUMMARY)**

### 🔹 **child**

The icon or widget inside FAB.

```dart
child: Icon(Icons.edit),
```

---

### 🔹 **backgroundColor**

```dart
backgroundColor: Colors.blue,
```

---

### 🔹 **foregroundColor**

Color of icon.

```dart
foregroundColor: Colors.white,
```

---

### 🔹 **onPressed()**

Action when clicked.

```dart
onPressed: () => print("Clicked!"),
```

---

### 🔹 **tooltip**

Shows text on long press.

```dart
tooltip: "Add Item",
```

---

### 🔹 **shape**

Change shape to rounded square or stadium.

```dart
shape: RoundedRectangleBorder(
  borderRadius: BorderRadius.circular(20),
),
```

---

### 🔹 **heroTag**

Used when navigating between screens.

```dart
heroTag: "uniqueTag",
```

---

---

# 🔥 **5. FloatingActionButton.extended()**

If you want **icon + label text**, use this:

```dart
FloatingActionButton.extended(
  onPressed: () {},
  icon: Icon(Icons.add),
  label: Text("Add Item"),
)
```

✔ Best for long text buttons
✔ Wide button
✔ Very useful for actions like: Add to cart, Upload, Save

---

# 🌈 **6. Mini FAB**

Smaller version:

```dart
FloatingActionButton(
  mini: true,
  child: Icon(Icons.camera),
  onPressed: () {},
)
```

---

# 🌟 **7. Multiple FABs (Speed Dial Style)**

Not directly supported → but can be created manually.

Simple example:

```dart
Column(
  mainAxisSize: MainAxisSize.min,
  children: [
    FloatingActionButton(
      mini: true,
      child: Icon(Icons.edit),
      onPressed: () {},
    ),
    SizedBox(height: 10),
    FloatingActionButton(
      mini: true,
      child: Icon(Icons.delete),
      onPressed: () {},
    ),
  ],
)
```

---

# 📌 **8. Place FAB at Different Positions**

By default FAB is bottom-right,
But use `floatingActionButtonLocation`:

```dart
floatingActionButtonLocation:
    FloatingActionButtonLocation.centerDocked,
```

Options include:

| Position       | Meaning                |
| -------------- | ---------------------- |
| `endFloat`     | Bottom-right (default) |
| `centerDocked` | Bottom-center          |
| `startFloat`   | Bottom-left            |
| `centerFloat`  | Center but floating    |

---

# 🎯 **9. FAB with Bottom Navigation Bar**

```dart
Scaffold(
  bottomNavigationBar: BottomAppBar(
    shape: CircularNotchedRectangle(),
  ),
  floatingActionButton: FloatingActionButton(
    onPressed: () {},
    child: Icon(Icons.add),
  ),
  floatingActionButtonLocation:
      FloatingActionButtonLocation.centerDocked,
)
```

---

# 💡 Quick Memory Tip

### ➕ FAB = Main Action Button

👉 Always used for most important action on the screen
👉 Circular, floating, attractive

---

