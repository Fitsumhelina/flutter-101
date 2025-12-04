

# 🎯 **NOTES – AppBar in Flutter**

`AppBar` is the **top bar** of a mobile app screen.
It usually contains:
✔ Title
✔ Icons
✔ Actions
✔ Background color
✔ Navigation button (Back button)
✔ Tabs (with TabBar)

---

# 🌟 1. What is AppBar?

`AppBar` is a built-in Flutter widget used inside a **Scaffold** to display the application toolbar.

```dart
Scaffold(
  appBar: AppBar(
    title: Text("Home"),
  ),
)
```

---

# 🧱 2. Where is AppBar used?

✔ In almost every screen
✔ For headings
✔ To show navigation icons
✔ For menus, search, profile icons
✔ For tabs (TabBar)
✔ For actions like settings, logout, notifications

---

# 🎨 3. AppBar Basic Structure

```dart
AppBar(
  title: Text("My App"),
  backgroundColor: Colors.blue,
  centerTitle: true,
)
```

---

# ✨ 4. Important AppBar Properties (SMART LIST)

## 1️⃣ **title**

The main heading.

```dart
title: Text("Dashboard"),
```

---

## 2️⃣ **backgroundColor**

Controls color of AppBar.

```dart
backgroundColor: Colors.teal,
```

---

## 3️⃣ **centerTitle**

Centers the title (iOS style).

```dart
centerTitle: true,
```

---

## 4️⃣ **leading**

Widget on the **left side**.

Examples:

* Back button
* Menu button (drawer)
* Profile picture

```dart
leading: Icon(Icons.menu),
```

Flutter shows a back button automatically when using Navigator.

---

## 5️⃣ **actions**

Widgets on **right side** (list).

Example:

```dart
actions: [
  Icon(Icons.notifications),
  SizedBox(width: 10),
],
```

You can add:
✔ search icon
✔ settings
✔ logout
✔ cart
✔ profile

---

## 6️⃣ **elevation**

Shadow under AppBar (default = 4)

```dart
elevation: 0, // flat (no shadow)
```

---

## 7️⃣ **shape**

Used to curve AppBar bottom edges.

```dart
shape: RoundedRectangleBorder(
  borderRadius: BorderRadius.vertical(bottom: Radius.circular(20)),
),
```

---

## 8️⃣ **toolbarHeight**

Increase AppBar height.

```dart
toolbarHeight: 80,
```

---

## 9️⃣ **leadingWidth**

Control size of leading widget.

```dart
leadingWidth: 70,
```

---

## 🔟 **flexibleSpace**

Add background gradient/image.

```dart
flexibleSpace: Container(
  decoration: BoxDecoration(
    gradient: LinearGradient(
      colors: [Colors.blue, Colors.purple],
    ),
  ),
),
```

---

# 🌈 5. Full AppBar Example (Beautiful UI)

```dart
AppBar(
  title: Text("Profile"),
  backgroundColor: Colors.deepPurple,
  centerTitle: true,
  elevation: 5,
  leading: Icon(Icons.arrow_back),
  actions: [
    Icon(Icons.settings),
    SizedBox(width: 10),
  ],
  shape: RoundedRectangleBorder(
    borderRadius: BorderRadius.vertical(bottom: Radius.circular(20)),
  ),
)
```

---

# 🔥 6. AppBar with Search Button

```dart
AppBar(
  title: Text("Products"),
  actions: [
    IconButton(
      icon: Icon(Icons.search),
      onPressed: () {},
    ),
  ],
)
```

---

# 📌 7. Transparent AppBar

```dart
AppBar(
  backgroundColor: Colors.transparent,
  elevation: 0,
)
```

Useful for splash screen/music apps.

---

# 🎯 8. AppBar with Tabs (TabBar)

```dart
AppBar(
  title: Text("Tabs Example"),
  bottom: TabBar(
    tabs: [
      Tab(text: "Home"),
      Tab(text: "Settings"),
    ],
  ),
)
```

---

# 🧠 Quick Summary (Memory Boost)

| Feature           | Purpose                 |
| ----------------- | ----------------------- |
| **title**         | AppBar title text       |
| **leading**       | Left widget (menu/back) |
| **actions**       | Right widgets           |
| **elevation**     | Shadow                  |
| **shape**         | Curve bottom            |
| **centerTitle**   | Center the title        |
| **flexibleSpace** | Gradient or image       |

