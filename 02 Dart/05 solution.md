

## 1️⃣ Create variables & print formatted sentence

```dart
void main(){
  String name = "Rahul";
  int age = 22;
  double height = 5.9;
  bool isStudent = true;

  print("My name is $name, I am $age years old, height is $height ft and student: $isStudent");
}
```

---

## 2️⃣ Convert int → double & double → int

```dart
void main(){
  int a = 10;
  double b = 12.75;

  double intToDouble = a.toDouble();
  int doubleToInt = b.toInt();

  print(intToDouble);  // 10.0
  print(doubleToInt);  // 12
}
```

---

## 3️⃣ Print first 3 characters of string

```dart
void main(){
  String text = "Flutter";
  print(text.substring(0,3)); // Flu
}
```

---

---

## 4️⃣ Perform arithmetic operations

```dart
void main(){
  int x = 12, y = 4;
  print("Sum: ${x+y}");
  print("Difference: ${x-y}");
  print("Multiplication: ${x*y}");
  print("Division: ${x/y}");
}
```

---

## 5️⃣ Concatenate first & last name

```dart
void main(){
  String firstName = "Aman";
  String lastName = "Kumar";
  
  print(firstName + " " + lastName);
}
```

---

## 6️⃣ String operations

```dart
void main(){
  String text = "Dart Programming";
  
  print(text.length);
  print(text.toUpperCase());
  print(text.toLowerCase());
}
```

---

---

## 7️⃣ List add & remove country

```dart
void main(){
  List countries = ["India", "USA", "Japan", "Nepal", "China"];
  
  print("Before: $countries");
  countries.add("Canada");
  countries.remove("Japan");

  print("After: $countries");
}
```

---

## 8️⃣ Find largest & smallest without min/max

```dart
void main(){
  List numbers = [12, 45, 7, 30, 19];

  int largest = numbers[0];
  int smallest = numbers[0];

  for(int n in numbers){
    if(n > largest) largest = n;
    if(n < smallest) smallest = n;
  }

  print("Largest: $largest");
  print("Smallest: $smallest");
}
```

---

## 9️⃣ Update map value

```dart
void main(){
  Map user = {"name":"Alex","age":20,"city":"Delhi"};

  print("Before: $user");
  user["city"] = "Mumbai";
  print("After: $user");
}
```

---

---

## 🔟 Square function

```dart
int square(int n) => n * n;

void main(){
  print(square(6)); // 36
}
```

---

## 1️⃣1️⃣ Greet user function

```dart
void greetUser(String name){
  print("Welcome $name!");
}

void main(){
  greetUser("Rahul");
}
```

---

## 1️⃣2️⃣ Multiply function

```dart
int multiply(int a, int b){
  return a * b;
}

void main(){
  print(multiply(4, 5)); // 20
}
```

---

---

## 1️⃣3️⃣ Student marks condition

```dart
void main(){
  int marks = 78;

  if(marks >= 90) print("Outstanding");
  else if(marks >= 75) print("Excellent");
  else if(marks >= 50) print("Good");
  else print("Needs Improvement");
}
```

---

## 1️⃣4️⃣ Table of 5

```dart
void main(){
  for(int i = 1; i <= 10; i++){
    print("5 x $i = ${5*i}");
  }
}
```

---

## 1️⃣5️⃣ For-each loop print colors

```dart
void main(){
  List colors = ["Red","Green","Blue","Yellow"];

  colors.forEach((c) => print(c));
}
```

---
**All 15 Class & Object Practice Problems SOLVED** in Dart.


---

# 🔹 **Level 1 — Basic Object Creation**

---

### 1. Book Class

```dart
class Book {
  String title, author;
  double price;

  Book(this.title, this.author, this.price);
}

void main() {
  var b1 = Book("Flutter Guide", "John", 299.0);
  var b2 = Book("Dart Basics", "Alex", 199.0);

  print("${b1.title} by ${b1.author} — ₹${b1.price}");
  print("${b2.title} by ${b2.author} — ₹${b2.price}");
}
```

---

### 2. Laptop Class

```dart
class Laptop {
  String brand;
  int ram;

  Laptop(this.brand, this.ram);

  void showSpecs() => print("Brand: $brand | RAM: ${ram}GB");
}

void main() {
  var l1 = Laptop("Dell", 8);
  l1.showSpecs();
}
```

---

### 3. Teacher Class

```dart
class Teacher {
  String name, subject;
  double salary;

  Teacher(this.name, this.subject, this.salary);
}

void main() {
  var t = Teacher("Riya", "Maths", 45000);
  print("Teacher: ${t.name} | Subject: ${t.subject} | Salary: ₹${t.salary}");
}
```

---

### 4. Dog Class

```dart
class Dog {
  String name, breed;

  Dog(this.name, this.breed);

  void bark() => print("$name is barking!");
}

void main() {
  var dog = Dog("Bruno", "Labrador");
  dog.bark();
}
```

---

### 5. Movie Class

```dart
class Movie {
  String name;
  double rating;

  Movie(this.name, this.rating);

  void review() => print(rating > 7 ? "Hit" : "Flop");
}

void main() {
  var m = Movie("KGF", 8.5);
  m.review();
}
```

---

# 🔹 Level 2 — Constructors

---

### 6. Person Class

```dart
class Person {
  String name;
  int age;

  Person(this.name, this.age);
}

void main() {
  var p1 = Person("Aman", 21);
  var p2 = Person("Rekha", 30);

  print("${p1.name}, Age: ${p1.age}");
  print("${p2.name}, Age: ${p2.age}");
}
```

---

### 7. Mobile + Discount

```dart
class Mobile {
  String model;
  double price;

  Mobile(this.model, this.price);

  void discount() => print("Discount Price: ${price - price*0.10}");
}

void main() {
  var m = Mobile("Samsung A52", 20000);
  m.discount();
}
```

---

### 8. Car Age Calculator

```dart
class Car {
  String brand;
  int year;

  Car(this.brand, this.year);

  void carAge() {
    int age = 2024 - year;
    print("Car Age: $age years");
  }
}

void main() {
  Car("Toyota", 2019).carAge();
}
```

---

### 9. Bank Account

```dart
class BankAccount {
  double balance;

  BankAccount(this.balance);

  void deposit(int amount) {
    balance += amount;
    print("Updated Balance: $balance");
  }
}

void main() {
  var acc = BankAccount(1000);
  acc.deposit(500);
}
```

---

### 10. Total Marks

```dart
class Student {
  int m1, m2, m3;

  Student(this.m1, this.m2, this.m3);

  int totalMarks() => m1 + m2 + m3;
}

void main() {
  var s = Student(78, 85, 92);
  print("Total Marks = ${s.totalMarks()}");
}
```

---

# 🔹 Level 3 — Methods & Multiple Objects

---

### 11. Circle Area

```dart
class Circle {
  double radius;

  Circle(this.radius);

  double area() => 3.14 * radius * radius;
}

void main() {
  print("Area = ${Circle(5).area()}");
}
```

---

### 12. Product with GST

```dart
class Product {
  String name;
  double price;

  Product(this.name, this.price);

  void applyGST() => print("Final Price = ${price + price*0.18}");
}

void main() {
  Product("Watch", 2000).applyGST();
}
```

---

### 13. Bus Available Seats

```dart
class Bus {
  int seats;
  String route;

  Bus(this.seats, this.route);

  int availableSeats(int booked) => seats - booked;
}

void main() {
  print("Seats Left = ${Bus(50, "City Express").availableSeats(18)}");
}
```

---

### 14. Employee Increment

```dart
class Employee {
  String name;
  double salary;

  Employee(this.name, this.salary);

  void increment(double percent) {
    salary += salary * percent / 100;
    print("New Salary = $salary");
  }
}

void main() {
  Employee("Rohan", 40000).increment(10);
}
```

---

### 15. Shop Bill Amount

```dart
class Shop {
  String productName;
  int quantity;
  double price;

  Shop(this.productName, this.quantity, this.price);

  double billAmount() => quantity * price;
}

void main() {
  var s = Shop("Notebook", 5, 30);
  print("Total Bill = ₹${s.billAmount()}");
}
```

---

---
 **Complete Answers for All 15 OOP Practice Questions** in Dart 


---

# 🔹 **1. Encapsulation — Bank**

```dart
class Bank {
  double _balance = 0;    // private

  void deposit(double amount) {
    _balance += amount;
  }

  void withdraw(double amount) {
    if(amount <= _balance) _balance -= amount;
    else print("Insufficient Balance");
  }

  double get balance => _balance;   // getter
}

void main() {
  var b = Bank();
  b.deposit(500);
  b.withdraw(200);
  print("Balance = ${b.balance}");
}
```

---

### 2. Student with Getter & Setter

```dart
class Student {
  String _name;
  int _marks;

  Student(this._name, this._marks);

  set marks(int m) {
    if(m <= 100) _marks = m;
    else print("Invalid Marks!");
  }

  String get name => _name;
  int get marks => _marks;
}

void main() {
  var s = Student("Ritik", 90);
  s.marks = 105; // error
  print("${s.name} scored ${s.marks}");
}
```

---

### 3. Temperature Conversion

```dart
class Temperature {
  double _celsius;

  Temperature(this._celsius);

  double get celsius => _celsius;

  double toFahrenheit() => (_celsius * 9/5) + 32;
}

void main() {
  var t = Temperature(30);
  print("${t.celsius}°C = ${t.toFahrenheit()}°F");
}
```

---

# 🔹 **4–7 Inheritance**

---

### 4. Device → Laptop

```dart
class Device {
  void powerOn() => print("Device Powered On");
}

class Laptop extends Device {
  void boot() => print("Laptop Booting...");
}

void main() {
  var l = Laptop();
  l.powerOn();
  l.boot();
}
```

---

### 5. Employee → Manager Salary

```dart
class Employee {
  String name;
  double salary;
  Employee(this.name, this.salary);
}

class Manager extends Employee {
  double bonus;
  Manager(name,salary,this.bonus): super(name,salary);

  double totalSalary() => salary + bonus;
}

void main() {
  var m = Manager("John",40000,8000);
  print("Total Salary = ${m.totalSalary()}");
}
```

---

### 6. Animal → Cat

```dart
class Animal {
  void eat() => print("Animal is eating");
}

class Cat extends Animal {
  void meow() => print("Cat says Meow");
}

void main() {
  var c = Cat();
  c.eat();
  c.meow();
}
```

---

### 7. Shape → Rectangle & Circle

```dart
class Shape {
  void area() {}
}

class Rectangle extends Shape {
  double l,b;
  Rectangle(this.l,this.b);

  @override
  void area() => print("Rectangle Area = ${l*b}");
}

class Circle extends Shape {
  double r;
  Circle(this.r);

  @override
  void area() => print("Circle Area = ${3.14*r*r}");
}

void main(){
  Shape s1 = Rectangle(4,5);
  Shape s2 = Circle(3);

  s1.area();
  s2.area();
}
```

---

# 🔹 **8–10 Polymorphism**

---

### 8. Vehicle → Bike & Car

```dart
class Vehicle {
  void run() => print("Vehicle Running");
}

class Bike extends Vehicle {
  @override void run() => print("Bike Running Fast");
}

class Car extends Vehicle {
  @override void run() => print("Car Running Smooth");
}

void main(){
  Vehicle v = Bike();
  v.run();

  v = Car();
  v.run();
}
```

---

### 9. Payment with Override

```dart
class Payment { void pay(){} }

class UPI extends Payment {
  @override pay() => print("Paid via UPI");
}

class Card extends Payment {
  @override pay() => print("Paid using Card");
}

class Cash extends Payment {
  @override pay() => print("Cash Payment Done");
}

void main(){
  Payment p = Cash();
  p.pay();
}
```

---

### 10. Animal Polymorphism in List

```dart
class Animal { void sound(){} }

class Cow extends Animal { @override sound()=>print("Cow: Moo"); }
class Dog extends Animal { @override sound()=>print("Dog: Bark"); }
class Cat extends Animal { @override sound()=>print("Cat: Meow"); }

void main(){
  List<Animal> animals = [Cow(),Dog(),Cat()];

  for(var a in animals){
    a.sound();  // polymorphism
  }
}
```

---

# 🔹 **11–13 Abstraction**

---

### 11. Abstract Phone

```dart
abstract class Phone {
  void call();
}

class Android extends Phone {
  @override call()=>print("Calling using Android");
}

class iPhone extends Phone {
  @override call()=>print("Calling using iPhone");
}

void main(){
  Phone p = iPhone();
  p.call();
}
```

---

### 12. Abstract Shape

```dart
abstract class Shape { double area(); }

class Triangle extends Shape {
  double b,h;
  Triangle(this.b,this.h);
  @override area()=>print("Area = ${(b*h)/2}");
}

class Square extends Shape {
  double s;
  Square(this.s);
  @override area()=>print("Area = ${s*s}");
}

void main(){
  Shape t = Triangle(6,4);
  Shape sq = Square(5);

  t.area();
  sq.area();
}
```

---

### 13. Account → SavingAccount

```dart
abstract class Account {
  void deposit(double amount);
  void withdraw(double amount);
}

class SavingAccount extends Account {
  double balance=0;

  @override deposit(amount)=> balance+=amount;

  @override withdraw(amount){
    if(amount<=balance) balance-=amount;
    else print("Low balance!");
  }
}

void main(){
  var acc = SavingAccount();
  acc.deposit(1000);
  acc.withdraw(300);
  print("Balance = ${acc.balance}");
}
```

---

# 🔹 **14–15 Constructor + Static + Super**

---

### 14. Person → Employee using super()

```dart
class Person {
  String name;
  int age;
  Person(this.name,this.age);
}

class Employee extends Person {
  double salary;
  Employee(String n,int a,this.salary) : super(n,a);

  void display()=>print("$name | $age | $salary");
}

void main(){
  Employee("Ravi",25,35000).display();
}
```

---

### 15. Calculator with Static

```dart
class Calculator {
  static const pi = 3.14;
  static int add(int a,int b)=>a+b;
}

void main(){
  print(Calculator.add(10,5));
  print(Calculator.pi);
}
```

Here are **complete answers with explanations and Dart code** for all **15 Future practice questions** 🚀

---

# **📄 Basic Understanding**

### **1. What is a Future in Dart?**

A **Future** represents a value that will be available **later**, after a delay or async task completes.

---

### **2. Give an analogy of Future**

A Future is like **ordering clothes online** — you pay now, but the package arrives later.
You don't get the item instantly, but you *expect it in the future*.

---

### **3. Difference between Future vs async/await**

| Feature         | Meaning                                                      |
| --------------- | ------------------------------------------------------------ |
| **Future**      | Represents a value that will come later                      |
| **async/await** | Keywords used to *read* Futures in a clean, step-by-step way |

---

# 🧪 **Code Output Prediction**

### **4. Output**

```dart
print("A");
Future(() => print("B"));
print("C");
```

✔ `Future` is asynchronous → executes later

**Output:**

```
A
C
B
```

---

### 5. Output

```dart
Future.delayed(Duration(seconds: 1), (){
  print("Loaded");
});
print("Start");
```

**Output:**

```
Start
Loaded
```

(Loaded prints after 1 second delay)

---

### 6. Will it wait? What is printed?

```dart
Future<String> getName() {
  return Future.delayed(Duration(seconds: 2), () => "Alex");
}

void main(){
  print(getName());
}
```

👉 It will **NOT** wait — it prints the *Future object*, not the value.

**Output:**

```
Instance of 'Future<String>'
```

---

# 🛠 Coding Tasks

### **7. Future returning "Sunny" after 2 seconds**

```dart
Future<String> fetchWeather() {
  return Future.delayed(Duration(seconds: 2), () => "Sunny");
}
```

---

### **8. async + await output**

```
Start
Fetching Data...
Data Loaded!
End
```

```dart
Future<void> main() async {
  print("Start");
  print("Fetching Data...");
  await Future.delayed(Duration(seconds: 2));
  print("Data Loaded!");
  print("End");
}
```

---

### **9. Future returning marks after 3 seconds**

```dart
Future<int> getMarks() {
  return Future.delayed(Duration(seconds: 3), () => 88);
}

void main() async {
  print(await getMarks());
}
```

---

### **10. Using .then() instead of await**

```
Reading File...
File Read Complete!
```

```dart
Future<String> readFile() {
  return Future.delayed(Duration(seconds: 1), () => "File Read Complete!");
}

void main() {
  print("Reading File...");
  readFile().then((value) => print(value));
}
```

---

### **11. Payment processing Future**

```dart
Future<void> processPayment() {
  return Future.delayed(Duration(seconds: 4), 
      () => print("Payment Successful"));
}
```

---

# 🔥 Slight Advanced

### **12. Future with try/catch throwing Server Error**

```dart
Future<void> loadServer() async {
  try {
    throw "Server Error";
  } catch(e) {
    print(e);
  }
}
```

---

### **13. Run two Futures using Future.wait()**

```dart
Future<void> main() async {
  var result = await Future.wait([
    Future.delayed(Duration(seconds: 1), () => "Task 1 Done"),
    Future.delayed(Duration(seconds: 2), () => "Task 2 Done"),
  ]);

  print(result);
}
```

**Output after 2 sec:**

```
[Task 1 Done, Task 2 Done]
```

---

### **14. Convert .then() → async/await**

```dart
void main() async {
  print(await getUser());
}
```

---

### **15. Future Chain example**

```
Data received
Error (if any)
Process Finished
```

```dart
Future<String> getData(){
  return Future.delayed(Duration(seconds: 1), () => "Data received");
}

void main() {
  getData()
  .then((value) => print(value))
  .catchError((e) => print("Error: $e"))
  .whenComplete(() => print("Process Finished"));
}
```

---

If you want, I can give you **20 more advanced async-Future questions** with tasks using:

✔ Future Streams
✔ Timeout
✔ Multiple async calls
✔ Error handling

Just reply **"Next Level Futures"** 🚀🔥
