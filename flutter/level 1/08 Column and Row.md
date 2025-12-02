

# **📌 Diagram (Column vs Row – Main Axis & Cross Axis)**

```
====================  COLUMN  ====================

          Cross Axis (horizontal)
        <------------------------>

          ┌───────────────────┐
 Main     │     [ Widget ]    │
 Axis     │     [ Widget ]    │
(vertical)│     [ Widget ]    │
   ↓      │     [ Widget ]    │
          └───────────────────┘


======================   ROW   =====================

 Main Axis (horizontal)
 <------------------------------------------------->

 ┌─────────────────────────────────────────────────┐
 │  [ W ]   [ W ]   [ W ]   [ W ]                  │
 │                                                 │
 └─────────────────────────────────────────────────┘
         ↑
         Cross Axis (vertical)
```

---

# **📘 Explanation – How Column and Row Work**

## **1. Column**

A **Column** arranges widgets **vertically**, one under another.

### **Main Axis (Vertical)**

* Controls the **vertical direction**.
* Widgets are placed from **top to bottom**.
* Properties affecting this axis:

  * `mainAxisAlignment`
  * `mainAxisSize`

### **Cross Axis (Horizontal)**

* Affects how widgets are aligned **horizontally**.
* Properties affecting this axis:

  * `crossAxisAlignment`

### **Example**

```dart
Column(
  mainAxisAlignment: MainAxisAlignment.center,
  crossAxisAlignment: CrossAxisAlignment.start,
  children: [
    Text("Item 1"),
    Text("Item 2"),
    Text("Item 3"),
  ],
);
```

---

## **2. Row**

A **Row** arranges widgets **horizontally**, side by side.

### **Main Axis (Horizontal)**

* Controls the **left–to–right** arrangement.
* Properties affecting this axis:

  * `mainAxisAlignment`
  * `mainAxisSize`

### **Cross Axis (Vertical)**

* Controls vertical alignment of widgets.
* Properties affecting this axis:

  * `crossAxisAlignment`

### **Example**

```dart
Row(
  mainAxisAlignment: MainAxisAlignment.spaceAround,
  crossAxisAlignment: CrossAxisAlignment.center,
  children: [
    Icon(Icons.star),
    Icon(Icons.star),
    Icon(Icons.star),
  ],
);
```

---

# **📝 Summary Note**

| Widget     | Main Axis  | Cross Axis | Layout Direction |
| ---------- | ---------- | ---------- | ---------------- |
| **Column** | Vertical   | Horizontal | Top → Bottom     |
| **Row**    | Horizontal | Vertical   | Left → Right     |

* **Main Axis = direction widgets are placed.**
* **Cross Axis = perpendicular direction used for alignment.**

