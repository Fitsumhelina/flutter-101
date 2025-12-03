# **Stateful Widgets in Flutter**

## **1. Introduction**

* Flutter widgets are of two types:

  1. **StatelessWidget** – Widgets that do not change over time.
  2. **StatefulWidget** – Widgets that **can change dynamically** during runtime.
* **Stateful Widgets** are used when the UI needs to **update in response to events** like button clicks, user input, or asynchronous data.

---

## **2. Structure of StatefulWidget**

A **StatefulWidget** consists of **two classes**:

1. **The StatefulWidget class** – Immutable; defines the widget itself.
2. **The State class** – Mutable; contains the actual state and logic.

```dart
class MyWidget extends StatefulWidget {
  @override
  _MyWidgetState createState() => _MyWidgetState();
}

class _MyWidgetState extends State<MyWidget> {
  // Variables to hold state
  int counter = 0;

  // Function to update state
  void incrementCounter() {
    setState(() {
      counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        Text('Counter: $counter'),
        ElevatedButton(
          onPressed: incrementCounter,
          child: Text('Increment'),
        ),
      ],
    );
  }
}
```

---

## **3. Key Concepts**

### **3.1 setState()**

* Used to **notify Flutter** that the state has changed.
* Automatically triggers a **rebuild** of the widget with the updated state.
* Example:

```dart
setState(() {
  counter += 1;
});
```

### **3.2 Lifecycle of StatefulWidget**

1. `createState()` → Called when widget is inserted in the widget tree.
2. `initState()` → Called once when the state object is created.
3. `build()` → Called whenever the widget needs to be rendered.
4. `didUpdateWidget()` → Called when the widget is rebuilt with new configuration.
5. `dispose()` → Called when the widget is removed from the tree; used to release resources.

### **3.3 Difference Between Stateful and Stateless**

| Feature              | StatelessWidget | StatefulWidget         |
| -------------------- | --------------- | ---------------------- |
| Can change state?    | ❌ No            | ✅ Yes                  |
| Rebuilt on setState? | ❌ No            | ✅ Yes                  |
| Example              | Text, Icon      | Checkbox, Slider, Form |

---

## **4. When to Use StatefulWidget**

* When the widget **needs to respond to user interactions**.
* When the widget **depends on data that can change over time**.
* Examples:

  * Toggle buttons
  * Forms and input fields
  * Animations
  * Fetching and displaying dynamic data

---

## **5. Tips**

* Keep state **localized** to the widget that needs it.
* Avoid unnecessary use of StatefulWidget if a StatelessWidget suffices.
* Use **`setState()` carefully** to update only what is necessary.

---
