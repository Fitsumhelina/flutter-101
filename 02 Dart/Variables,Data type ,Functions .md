
# 📘 **DART BASICS – Smart Notes**

---

## 🌟 1. Variables

Used to store data (number, text, etc.)

```dart
var name = "John";      // dart decides type automatically
String city = "Delhi";  // explicitly typed
int age = 21;           // integer
double score = 85.5;    // decimal
bool isActive = true;   // true/false values
```

---

## 🔠 2. DATA TYPES

| Type     | Example                    | Use                   |
| -------- | -------------------------- | --------------------- |
| `String` | `"Hello"`                  | Words or text         |
| `int`    | `20`                       | Whole numbers         |
| `double` | `10.5`                     | Decimal values        |
| `bool`   | `true / false`             | Condition values      |
| `List`   | `[1,2,3]`                  | Store multiple values |
| `Map`    | `{"name":"Alex","age":20}` | Key-value data        |

Example:

```dart
String language = "Dart";
int year = 2025;
double price = 99.99;
bool available = false;
```

---

## ✍️ 3. String + Number Operations

```dart
String first = "Flutter";
String second = "Dart";
print(first + " & " + second);  // Output: Flutter & Dart

int a = 10;
int b = 5;
print(a + b);   // 15
print(a * b);   // 50
print(a / b);   // 2.0
```

---

## 📝 . Lists (Arrays)

Store multiple values. Can be dynamic or typed.

```dart
List<String> fruits = ["Apple", "Banana", "Mango"];
List<int> numbers = [1, 2, 3, 4];

fruits.add("Orange");      // Add element
fruits.remove("Banana");   // Remove element

print(fruits[0]);          // Access first element
print(numbers.length);     // Number of elements
```

---

## 🗝 . Maps (Key-Value Pairs)

```dart
Map<String, dynamic> user = {
  "name": "Alex",
  "age": 25,
  "isActive": true
};

print(user["name"]);       // Access value
user["city"] = "Delhi";    // Add new key-value
```

---

## 🔥 4. Functions

Block of code that performs work.

```dart
// Simple function
void greet() {
  print("Hello Developer!");
}

// With parameters
int add(int x, int y) {
  return x + y;
}

void main(){
  greet();
  print(add(5,10));  // Output: 15
}
```

---

## 🔀 5. Decision Making (IF/ELSE)

```dart
int marks = 75;

if(marks >= 80){
  print("Excellent");
}
else if(marks >= 50){
  print("Good");
}
else{
  print("Try again");
}
```

---

## 🔁 6. Loops

### 🔹 **For Loop**

```dart
for(int i=1; i<=5; i++){
  print("Count: $i");
}
```

### 🔹 **While Loop**

```dart
int n = 1;
while(n <= 3){
  print("Hello $n");
  n++;
}
```

---

## 🔄 7. For-Each Loop

Used to loop through Lists.

```dart
List fruits = ["Apple", "Banana", "Mango"];

for(String item in fruits){
  print(item);
}

// OR shorter
fruits.forEach((f) => print(f));
```

---

# 💡 Revision Summary (1 page)

| Feature   | Keyword            | Example            |
| --------- | ------------------ | ------------------ |
| Variable  | var / String / int | `var age=20;`      |
| String    | Text               | `"Hello"`          |
| Number    | int/double         | `int x=10;`        |
| Function  | void / return      | `add(5,10);`       |
| Condition | if / else          | `if(x>10){ }`      |
| Loop      | for / while        | `for(i=0;i<5;i++)` |
| For Each  | list iteration     | `fruits.forEach()` |

---
