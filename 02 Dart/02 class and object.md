

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


# 📘 **Practice Problems on Class & Object**

### 🔹 Level 1 — Basic Object Creation

1. Create a `Book` class with properties: `title`, `author`, `price`.
   Create two objects and print values.

2. Create a `Laptop` class with `brand` and `ram`.
   Make a method `showSpecs()` to display details.

3. Make a `Teacher` class with `name`, `subject`, `salary`.
   Create one object and print teacher details.

4. Create a `Dog` class with `name` and `breed`.
   Make method `bark()` → print `"Dog is barking!"`.

5. Create a class `Movie` with `name`, `rating(double)` and print `"Hit" if rating > 7 else Flop".

---

### 🔹 Level 2 — Constructors

6. Create a `Person` class with constructor to initialize `name` and `age`.
   Create two objects and show details.

7. Create `Mobile` class with constructor taking `model`, `price`.
   Add method `discount()` → print price - 10%.

8. Create `Car` class with `brand`, `year(int)`.
   Add method `carAge()` → print how old the car is.

9. Create a `BankAccount` class with property `balance`.
   Constructor sets balance and method `deposit(int amount)` updates it.

10. Make class `Student` with `marks1`, `marks2`, `marks3`.
    Create method `totalMarks()` and return sum.

---

### 🔹 Level 3 — Methods & Multiple Objects

11. Create a class `Circle` with `radius`.
    Method → `area()` = 3.14 * r * r.

12. Create a `Product` class with `name` and `price`.
    Method → `applyGST()` add 18% GST to price.

13. Create a `Bus` class with `seats`, `route`.
    Method → `availableSeats(int booked)` → return seats - booked.

14. Create `Employee` class with `name`, `salary`.
    Add method `increment(double percent)` → increase salary.

15. Create a `Shop` class with `productName`, `quantity`, `price`.
    Method → `billAmount()` = quantity * price.
