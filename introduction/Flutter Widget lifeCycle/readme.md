

# 🟡 1. Stateless Widget Lifecycle

A **Stateless widget has no state**, nothing changes inside it.

### Lifecycle is very simple:

```
Constructor → build() → finished
```

📌 Meaning:

| Step            | What happens      |
| --------------- | ----------------- |
| **Constructor** | Widget is created |
| **build()**     | UI is drawn once  |

That’s all.
It **does not rebuild unless parent widget refreshes it or app hot reloads.**

**Example of Stateless UI**
Text, Icon, Static Screen, App Title

---

# 🔵 2. Stateful Widget Lifecycle

A **Stateful widget can change over time** — button clicks, counters, animations, API data load, etc.

It has **two parts**:

| Part             | Role                                  |
| ---------------- | ------------------------------------- |
| `StatefulWidget` | UI blueprint                          |
| `State`          | Stores data/variables that can change |

---

### Full Lifecycle (simple diagram)

```
Constructor
     ↓
createState()
     ↓
initState()
     ↓
build()  ← (runs again every time setState() is called)
     ↑
setState()
     ↓
didUpdateWidget()   (runs only when widget config changes)
```

---

### 📝 What each part means

| Lifecycle Method      | Meaning                                                                        |
| --------------------- | ------------------------------------------------------------------------------ |
| **Constructor**       | Widget created                                                                 |
| **createState()**     | Creates a State object                                                         |
| **initState()**       | Runs once when widget is added to UI (good for API calls, timers, controllers) |
| **build()**           | Draws UI — runs many times                                                     |
| **setState()**        | Updates variables + rebuilds UI                                                |
| **didUpdateWidget()** | Called when parent updates widget (rare use but important)                     |

---

# 🧠 Understand With a Simple Example

Example: Counter App

* App starts → `createState()` → `initState()` → UI shows **0**
* User taps button → `setState()` → updates number
* `build()` runs again → UI shows **1**
* Taps again → UI rebuilds → **2**, **3**, ...

So **Stateful widget = can change and rebuild the UI**.

---

# 🔥 Quick Memory Notes (Very Important)

| Stateless                  | Stateful                                              |
| -------------------------- | ----------------------------------------------------- |
| No internal change         | Can change UI using setState()                        |
| Only constructor → build() | Has full lifecycle: initState, build, didUpdateWidget |
| Faster but less flexible   | Powerful and dynamic                                  |
| Use for static UI          | Use for dynamic UI (counters, forms, API data)        |

---

# Summary (keep in notebook)

```
Stateless:
  constructor → build → done

Stateful:
  constructor → createState → initState → build
  setState → rebuild UI
  didUpdateWidget → when widget updated externally
```

