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

- Controls the **vertical direction**.
- Widgets are placed from **top to bottom**.
- Properties affecting this axis:

  - `mainAxisAlignment`
  - `mainAxisSize`

### **Cross Axis (Horizontal)**

- Affects how widgets are aligned **horizontally**.
- Properties affecting this axis:

  - `crossAxisAlignment`

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

- Controls the **left–to–right** arrangement.
- Properties affecting this axis:

  - `mainAxisAlignment`
  - `mainAxisSize`

### **Cross Axis (Vertical)**

- Controls vertical alignment of widgets.
- Properties affecting this axis:

  - `crossAxisAlignment`

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

- **Main Axis = direction widgets are placed.**
- **Cross Axis = perpendicular direction used for alignment.**

# 🎯 **Notes – MainAxisAlignment, CrossAxisAlignment & MainAxisSize**

These properties are used inside **Row** and **Column** widgets to control **alignment and spacing**.

---

# 🧭 1. **Main Axis vs Cross Axis**

| Widget     | Main Axis (direction)     | Cross Axis (opposite)     |
| ---------- | ------------------------- | ------------------------- |
| **Row**    | Horizontal (left → right) | Vertical (top ↕ bottom)   |
| **Column** | Vertical (top → bottom)   | Horizontal (left ↔ right) |

📌 **Main axis = direction of children**
📌 **Cross axis = perpendicular direction**

---

# 1️⃣ **MainAxisAlignment**

Controls **HOW children are positioned along the main axis**.

### 📌 Used for:

`Row()`, `Column()`

---

## ✔ **Options**

### 1. **start**

Children start at the beginning.

```
|A B C          |
```

### 2. **center**

Children placed in center.

```
|    A B C      |
```

### 3. **end**

Children at the end.

```
|          A B C|
```

### 4. **spaceBetween**

Equal space **between** children.

```
|A    B    C|
```

### 5. **spaceAround**

Each child gets space **around** (half-size on edges).

```
|  A   B   C  |
```

### 6. **spaceEvenly**

Equal space **everywhere**.

```
|   A   B   C   |
```

---

# 2️⃣ **CrossAxisAlignment**

Controls alignment **across** the main axis (opposite direction).

---

## ✔ **Options**

### 1. **start**

Children aligned to the start of cross-axis.

Row → top
Column → left

### 2. **center**

Centered on cross-axis.

### 3. **end**

Aligned to the end of cross-axis.

Row → bottom
Column → right

### 4. **stretch**

Children stretch to fill cross-axis.

Example: In a Column → widgets fill full width.

---

# 3️⃣ **MainAxisSize**

Controls **how much space Row/Column takes** on the main axis.

| Value                          | Meaning                                |
| ------------------------------ | -------------------------------------- |
| **MainAxisSize.max** (default) | Takes full available space             |
| **MainAxisSize.min**           | Takes only required space for children |

---

### ✔ Example to understand:

### **MainAxisSize.max**

The Row/Column occupies ALL available space.

### **MainAxisSize.min**

The Row/Column shrinks to fit children only:

```
[ A B C ]
```

---

# 🧠 Quick Summary (1 Page Memory)

| Property               | Controls                        | Used in     | Options                                                    |
| ---------------------- | ------------------------------- | ----------- | ---------------------------------------------------------- |
| **mainAxisAlignment**  | Position along main axis        | Row, Column | start, center, end, spaceBetween, spaceAround, spaceEvenly |
| **crossAxisAlignment** | Position along cross axis       | Row, Column | start, center, end, stretch                                |
| **mainAxisSize**       | Size of Row/Column on main axis | Row, Column | min, max                                                   |



# Simple Example


```dart
Row(
  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
  crossAxisAlignment: CrossAxisAlignment.center,
  mainAxisSize: MainAxisSize.max,
  children: [
    Text("A"),
    Text("B"),
    Text("C"),
  ],
);
```
