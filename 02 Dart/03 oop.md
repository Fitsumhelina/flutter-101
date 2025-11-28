

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

# 📘 **OOP Practice Questions (15 Problems)**

### 🔹 Encapsulation

1. Create a class `Bank` with a private variable `_balance`.
   Add methods `deposit()` and `withdraw()`. Use getter to view balance.

2. Create a class `Student` with private properties `_name` and `_marks`.
   Use setter to update marks (only if marks ≤ 100) and getter to read both.

3. Create a class `Temperature` with private variable `_celsius`.
   Add a getter for Celsius and a method to convert to Fahrenheit.

---

### 🔹 Inheritance

4. Create a base class `Device` with method `powerOn()` and derived class `Laptop` that adds `boot()` method. Call both via object.

5. Create parent class `Employee` with name & salary.
   Child class `Manager` adds bonus. Print total salary.

6. Make class `Animal → Cat`.
   `Animal` has `eat()` method, `Cat` has `meow()`. Create an object and call both methods.

7. Create base class `Shape` with an empty `area()` method.
   Derived classes: `Rectangle` and `Circle`. Override area in each.

---

### 🔹 Polymorphism

8. Create `Vehicle` class with `run()`.
   Make `Bike` and `Car` override `run()` and print different messages.

9. Create class `Payment` with method `pay()`.
   Subclasses `UPI`, `Card`, `Cash` override `pay()` in different ways.

10. Write a program where `Animal` has sound(), subclasses `Cow`, `Dog`, `Cat` override it.
    Create a list of animals and use polymorphism to call sound().

---

### 🔹 Abstraction

11. Create `abstract class Phone` with method `call()`.
    Subclasses `Android` and `iPhone` must implement call().

12. Make `abstract class Shape` containing `area()`.
    Implement `Triangle` and `Square`.

13. Create abstract class `Account` with `deposit()` & `withdraw()`.
    Create class `SavingAccount` implementing logic.

---

### 🔹 Constructor + Static + Super

14. Create class `Person` with constructor(name, age).
    Create `Employee` class extending Person using `super()`.

15. Create `Calculator` class with a static method `add(a,b)` and static constant `pi`.
    Use without creating an object.

