

# 📘 **Object Oriented Programming (OOP) in Dart**

OOP is a programming style that organizes code using **classes & objects**—just like real-life models.

---

## 🔥 4 Pillars of OOP

| Pillar        | Meaning                                | Example Keyword       |
| ------------- | -------------------------------------- | --------------------- |
| Encapsulation | Wrap data + functions                  | class, private `_var` |
| Inheritance   | One class from another                 | `extends`             |
| Polymorphism  | Many forms, method override            | `@override`           |
| Abstraction   | Hiding details, showing only essential | `abstract class`      |

---

## 1️⃣ Encapsulation – Data + Methods Together

Protects data using getters & setters.

```dart
class BankAccount {
  double _balance = 0;     // Private variable (_)

  void deposit(double amount) {
    _balance += amount;
  }

  double get balance => _balance;  // Getter
}

void main() {
  var acc = BankAccount();
  acc.deposit(500);
  print(acc.balance);    // 500
}
```

---

## 2️⃣ Inheritance – Reuse Code

A child class inherits from parent class.

```dart
class Animal {
  void sound() => print("Animal makes sound");
}

class Dog extends Animal {
  void bark() => print("Dog barks");
}

void main() {
  var d = Dog();
  d.sound(); // from Animal
  d.bark();  // from Dog
}
```

---

## 3️⃣ Polymorphism – One Name, Many Behaviors

### 🔹 Method Overriding

```dart
class Shape {
  void draw() => print("Drawing shape");
}

class Circle extends Shape {
  @override
  void draw() => print("Drawing circle");
}

void main() {
  Shape s = Circle();   // polymorphism
  s.draw();             // Drawing circle
}
```

---

## 4️⃣ Abstraction – Hide Complexity

Use abstract class → cannot be directly instantiated.

```dart
abstract class Vehicle {
  void start();   // only declaration
}

class Car extends Vehicle {
  @override
  void start() => print("Car engine started");
}

void main() {
  Vehicle v = Car();  
  v.start();
}
```

---

# ✨ Extra OOP Concepts

---

### 🔹 Constructor Types

```dart
class Student {
  String name;

  Student(this.name);     // default constructor
  Student.guest() : name = "Guest";  // named constructor
}
```

---

### 🔹 `super` Keyword

Used to call parent class methods/variables.

```dart
class Parent {
  void show() => print("Parent method");
}

class Child extends Parent {
  @override
  void show() {
    super.show();     // calling parent method
    print("Child method");
  }
}
```

---

### 🔹 Static Keyword

Belongs to class, not objects.

```dart
class MathTool {
  static const pi = 3.14;
  static double square(num x) => x * x;
}

void main() {
  print(MathTool.pi);
  print(MathTool.square(5)); // 25
}
```

---

# 🧠 OOP Summary Table

| Concept       | Use                  | Keyword               |
| ------------- | -------------------- | --------------------- |
| Class         | Blueprint for object | `class`               |
| Object        | Instance of a class  | `var obj = Class();`  |
| Encapsulation | Data protection      | `_var`, getter/setter |
| Inheritance   | Reuse code           | `extends`             |
| Polymorphism  | Different behaviors  | `override`            |
| Abstraction   | Hide internal logic  | `abstract`            |
| Static        | Shared values        | `static`              |

---
