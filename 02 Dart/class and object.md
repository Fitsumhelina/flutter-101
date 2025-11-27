

# 📘 **Class & Object in Dart — Explained**

## 🔷 What is a Class?

A **class** is a blueprint or template used to create **objects**.
It defines **variables (properties)** and **functions (methods)** inside it.

Example:

```dart
class Car {
  String brand = "Toyota";   // property/variable
  int speed = 120;

  void showInfo(){           // method/function
    print("Brand: $brand, Speed: $speed km/h");
  }
}
```

---

## 🔷 What is an Object?

An **object** is created from a class.
It represents a **real-world instance** of that class.

```dart
void main(){
  Car myCar = Car();   // object created
  myCar.showInfo();    // calling method
}
```

📌 Output:

```
Brand: Toyota, Speed: 120 km/h
```

---

## 🧩 Why use Class & Object?

| Feature            | Meaning                           |
| ------------------ | --------------------------------- |
| Reusability        | One class → many objects          |
| Organized Code     | Data + functions grouped together |
| Real Life Modeling | Cars, Students, Products etc.     |

---

## 🏗 Creating object with custom values

```dart
class Student {
  String name = "";
  int age = 0;

  void introduce(){
    print("My name is $name and I am $age years old.");
  }
}

void main(){
  var s1 = Student();      // object 1
  s1.name = "Aman";
  s1.age = 18;

  s1.introduce();

  var s2 = Student();      // object 2
  s2.name = "Riya";
  s2.age = 20;

  s2.introduce();
}
```

---

## 🧱 Class with Constructor

A constructor sets initial values automatically when an object is created.

```dart
class Person {
  String name;
  int age;

  Person(this.name, this.age);  // constructor

  void show(){
    print("Name: $name, Age: $age");
  }
}

void main(){
  var p = Person("Rahul", 22);
  p.show();
}
```

Output:

```
Name: Rahul, Age: 22
```

---

## 🧠 Quick Summary

| Concept         | Meaning                 |
| --------------- | ----------------------- |
| **Class**       | Template/Blueprint      |
| **Object**      | Instance of class       |
| **Property**    | Variable inside class   |
| **Method**      | Function inside class   |
| **Constructor** | Auto initializes values |

---
