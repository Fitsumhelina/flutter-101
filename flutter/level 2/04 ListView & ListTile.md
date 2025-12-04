

# 📘 **NOTE – ListView & ListTile in Flutter**

---

# 🎯 **1. What is ListView?**

`ListView` is a scrollable column of items.

✔ Shows items vertically
✔ Auto scrolls when content exceeds screen
✔ Used in chats, settings, contacts, menus, etc.

---

## 📌 Basic Example

```dart
ListView(
  children: [
    Text("Item 1"),
    Text("Item 2"),
    Text("Item 3"),
  ],
)
```

---

# ⭐ **2. Types of ListView**

### 1️⃣ **ListView()** — default with children

```dart
ListView(
  children: [...],
)
```

---

### 2️⃣ **ListView.builder()**

Used when list is long or dynamic.

```dart
ListView.builder(
  itemCount: 50,
  itemBuilder: (context, index) {
    return Text("Item $index");
  },
)
```

✔ Best for long lists
✔ Efficient (creates items only when visible)

---

### 3️⃣ **ListView.separated()**

Adds spacing or divider between items.

```dart
ListView.separated(
  itemCount: 5,
  itemBuilder: (context, index) => Text("Item $index"),
  separatorBuilder: (context, index) => Divider(),
)
```

---

---

# 🧱 **3. What is ListTile?**

`ListTile` is a ready-made UI widget for list items.

You get:

* Icon on left
* Big title
* Subtitle
* Trailing icon
* Tap ripple effect

Perfect for settings menus, app menus, contacts, chats.

---

## 📌 Basic ListTile Example

```dart
ListTile(
  leading: Icon(Icons.person),
  title: Text("John Doe"),
  subtitle: Text("Online"),
  trailing: Icon(Icons.call),
)
```

---

# ⭐ **4. ListTile Properties (Smart Summary)**

### 🔹 **leading**

Widget on left (icon/image).

```dart
leading: Icon(Icons.account_circle),
```

---

### 🔹 **title**

Main text.

```dart
title: Text("Settings"),
```

---

### 🔹 **subtitle**

Smaller text under title.

```dart
subtitle: Text("Account, Privacy, Security"),
```

---

### 🔹 **trailing**

Widget on right.

```dart
trailing: Icon(Icons.arrow_forward_ios),
```

---

### 🔹 **onTap**

Click action.

```dart
onTap: () {
  print("Tapped!");
},
```

---

### 🔹 **contentPadding**

Spacing inside tile.

```dart
contentPadding: EdgeInsets.all(10),
```

---

---

# 🌟 **5. ListView + ListTile Together**

Most common usage:

```dart
ListView(
  children: [
    ListTile(
      leading: Icon(Icons.home),
      title: Text("Home"),
      trailing: Icon(Icons.arrow_forward_ios),
    ),
    ListTile(
      leading: Icon(Icons.settings),
      title: Text("Settings"),
    )
  ],
)
```

---

---

# 🔥 **6. ListView.builder + ListTile (Professional Use)**

```dart
ListView.builder(
  itemCount: users.length,
  itemBuilder: (context, index) {
    return ListTile(
      leading: CircleAvatar(
        child: Text(users[index][0]),
      ),
      title: Text(users[index]),
      trailing: Icon(Icons.arrow_forward),
    );
  },
)
```

---

# 💡 **7. ListTile with Image**

```dart
ListTile(
  leading: CircleAvatar(
    backgroundImage: NetworkImage("https://example.com/user.jpg"),
  ),
  title: Text("Alex"),
  subtitle: Text("Active now"),
)
```

---

# 📌 **8. Making ListTile Rounded**

```dart
ListTile(
  shape: RoundedRectangleBorder(
    borderRadius: BorderRadius.circular(15),
  ),
  tileColor: Colors.grey[200],
  title: Text("Notifications"),
)
```

---

# 🎯 **9. When to use What?**

| Widget                 | Use Case                                     |
| ---------------------- | -------------------------------------------- |
| **ListView**           | Scrollable list                              |
| **ListView.builder**   | Long/dynamic list                            |
| **ListTile**           | Beautiful list item with icon/title/subtitle |
| **ListView.separated** | Items with spacing/divider                   |

---

# 🧠 **Quick Memory Tip**

**ListView = Scroll
ListTile = Item design**

