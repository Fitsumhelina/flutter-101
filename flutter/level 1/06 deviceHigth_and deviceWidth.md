
### **Getting Device Height and Width in Flutter**

In Flutter, you can get the device’s **screen dimensions** using `MediaQuery`.

**Example:**

```dart
import 'package:flutter/material.dart';

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    // Get screen width and height
    double screenWidth = MediaQuery.of(context).size.width;
    double screenHeight = MediaQuery.of(context).size.height;

    return Scaffold(
      appBar: AppBar(title: Text('Smart Notes')),
      body: Center(
        child: Text(
          'Width: $screenWidth\nHeight: $screenHeight',
          textAlign: TextAlign.center,
        ),
      ),
    );
  }
}
```

Here:

* `MediaQuery.of(context).size.width` → the **width** of the device screen.
* `MediaQuery.of(context).size.height` → the **height** of the device screen.

---

### **Using Height & Width for Responsive Layouts**

1. **Proportional Sizing**
   Instead of hardcoding pixels, use a **percentage of screen size**.

```dart
Container(
  width: screenWidth * 0.9,   // 90% of screen width
  height: screenHeight * 0.2, // 20% of screen height
  color: Colors.blue,
)
```

2. **SafeArea + MediaQuery**
   Even with `SafeArea`, you might want to **subtract unsafe areas**:

```dart
double safeHeight = MediaQuery.of(context).size.height - MediaQuery.of(context).padding.top - MediaQuery.of(context).padding.bottom;
```

3. **Font & padding scaling**
   You can scale text or spacing based on screen width/height for consistent look on all devices.

---

### **Example in a Smart Notes App**

Suppose you want a note card that is **full width but has some margin**, and height is proportional to screen height:

```dart
Container(
  width: screenWidth * 0.95,
  height: screenHeight * 0.15,
  margin: EdgeInsets.symmetric(vertical: 8.0),
  padding: EdgeInsets.all(16.0),
  decoration: BoxDecoration(
    color: Colors.yellow[100],
    borderRadius: BorderRadius.circular(12),
  ),
  child: Column(
    crossAxisAlignment: CrossAxisAlignment.start,
    children: [
      Text('Note Title', style: TextStyle(fontSize: screenWidth * 0.05)),
      SizedBox(height: 8),
      Text('Note content goes here...', style: TextStyle(fontSize: screenWidth * 0.04)),
    ],
  ),
)
```

* `screenWidth * 0.95` → 95% of device width
* `screenHeight * 0.15` → 15% of device height
* Font sizes are scaled using `screenWidth` for consistency.

---

✅ **Key Takeaways:**

* Always use `MediaQuery` for **responsive sizing**.
* Combine **SafeArea** with screen dimensions to avoid overlapping system UI.
* Avoid hardcoding sizes; proportional sizing works better across devices.

---
