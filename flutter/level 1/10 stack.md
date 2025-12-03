
# 🎯 **NOTES – Stack in Flutter**

`Stack` is a Flutter widget that lets you **place widgets on top of each other** (like layers).

Think of it like:
🧁 *Cake layers*
📱 *Instagram story UI (text over image)*
🗺 *Floating button over map*

---

# 🌟 1. What is Stack?

A **Stack** arranges widgets **one on top of another**.

```dart
Stack(
  children: [
    Widget1, // bottom layer
    Widget2, // middle
    Widget3, // top layer
  ],
)
```

Order = **bottom → top**

---

# 🌈 2. Why use Stack?

✔ Show text over images
✔ Create overlapping widgets
✔ Build custom UI designs
✔ Position widgets freely
✔ Build badges, floating buttons, banners

---

# 📌 3. Basic Example

```dart
Stack(
  children: [
    Container(width: 200, height: 200, color: Colors.blue),
    Text("Hello", style: TextStyle(fontSize: 25, color: Colors.white)),
  ],
);
```

Output: text appears **on top** of the blue box.

---

# 🎯 4. Using Positioned in Stack

`Positioned` lets you place widgets exactly where you want.

```dart
Stack(
  children: [
    Container(width: 200, height: 200, color: Colors.green),

    Positioned(
      top: 10,
      left: 10,
      child: Text("Top Left"),
    ),

    Positioned(
      bottom: 10,
      right: 10,
      child: Text("Bottom Right"),
    ),
  ],
)
```

---

# 🔥 5. Stack Properties (Very Important)

### ✔ 1. `alignment`

Aligns all children inside the stack.

```dart
Stack(
  alignment: Alignment.center,
  children: [...]
)
```

### ✔ 2. `fit`

Controls how non-positioned widgets behave.

Options:

* `StackFit.loose` → children keep natural size (default)
* `StackFit.expand` → children fill entire stack

### ✔ 3. `clipBehavior`

Controls if children outside stack should be visible.

* `Clip.none` → allow overflow
* `Clip.hardEdge` / `Clip.antiAlias` → crop children

---

# 🧠 6. Positioned vs Non-Positioned Widgets

| Type                     | Example               | Behavior                     |
| ------------------------ | --------------------- | ---------------------------- |
| **Non-positioned child** | `Container()`         | Follows alignment property   |
| **Positioned child**     | `Positioned(top: 10)` | Follows provided coordinates |

---

# 🌟 7. Common Real-Life Uses of Stack

✔ Profile avatar with status dot
✔ Image with title text
✔ Floating buttons
✔ Card with badge
✔ Custom login screens
✔ Splash screens
✔ Maps with markers

---

# 📸 8. Real UI Example

```dart
Stack(
  children: [
    Image.asset("assets/bg.jpg", width: double.infinity, height: 300, fit: BoxFit.cover),

    Positioned(
      bottom: 20,
      left: 20,
      child: Text(
        "Welcome",
        style: TextStyle(fontSize: 30, color: Colors.white),
      ),
    ),
  ],
);
```

---

# 🧠 Quick Summary

| Concept          | Meaning                                 |
| ---------------- | --------------------------------------- |
| **Stack**        | Overlap widgets (one on top of another) |
| **children**     | List of widgets in layer order          |
| **Positioned**   | Absolute position control               |
| **alignment**    | Align non-positioned children           |
| **fit**          | Expand or keep natural size             |
| **clipBehavior** | Control overflow                        |

---

