# 🔥 What is **Future** in Dart?

A **Future** represents a value that will be available **in the future**, not immediately.

### 📌 In simple words:

> Future = Result that comes **later**, like a promise.

---

### 🧠 **Analogy to Understand Easily**

Imagine you order a **pizza** online 🍕.

1. You place an order → **Request sent**
2. You continue watching TV → **Program keeps running**
3. After some time, pizza arrives → **Future returns result**

You don’t sit at the door waiting.
You do other work **until the delivery happens** — this is how **Future** works!

---

### 🎯 A Future in Dart is used for:

| Works done later    | Examples              |
| ------------------- | --------------------- |
| Network/API request | Fetching user data    |
| Database read/write | Saving login info     |
| Delay/Timer         | Splash screen loading |
| File handling       | Reading local files   |

---

# 🧪 Example of Future without async/await

```dart
Future<String> getData() {
  return Future.delayed(Duration(seconds: 2), () {
    return "Data Loaded";
  });
}

void main() {
  print("Start");
  var result = getData();
  print(result);  
  print("End");
}
```

### Output:

```
Start
Instance of 'Future<String>'
End
```

Because the result comes **after 2 seconds**, but `main()` continues running.

---

# 📌 Now Let's Fix it using **async** & **await**

```dart
Future<String> getData() async {
  await Future.delayed(Duration(seconds: 2));
  return "Data Loaded Successfully";
}

void main() async {
  print("Start");
  String data = await getData();
  print(data);
  print("End");
}
```

### Output:

```
Start
Data Loaded Successfully
End
```

Now the program **waits** for Future to complete before printing.

---

# 🔥 Difference Between `Future`, `async` & `await`

| Term     | Meaning                        | Example                  |
| -------- | ------------------------------ | ------------------------ |
| `Future` | A task that finishes in future | `Future<String>`         |
| `async`  | Makes a function asynchronous  | `Future func() async {}` |
| `await`  | Waits for Future to complete   | `await getData()`        |

### 📌 Easy Analogy

| Real Life                   | Dart                     |
| --------------------------- | ------------------------ |
| Ordering pizza              | Calling Future function  |
| Chef cooks for 20 minutes   | Future takes time        |
| You wait when food is ready | `await` waits for result |
| "Food ready, eat!"          | Future returns value     |

---

# 💡 Key Notes (Very Important)

✔ `Future` returns value **later**, not instantly
✔ `async` is used to **create** a function that waits or runs slowly
✔ `await` **pauses** execution until Future is done
✔ You can only use `await` inside an `async` function
✔ Useful for API calls, file read/write, timers, etc.

---

# 🔥 Final Short Example (Perfect Revision)

```dart
Future<void> downloadFile() async {
  print("Downloading...");
  await Future.delayed(Duration(seconds: 3));
  print("Download complete!");
}

void main() async {
  print("Task Started");
  await downloadFile();      // waits for 3 seconds
  print("Task Finished");
}
```

---


#  **15 Dart Future Practice Questions**

### 📄 Basic Understanding

1. What is a Future in Dart? Explain in one or two lines.
2. Write an analogy of Future (different from pizza example).
3. What is the difference between Future and async/await?

---

### 🧪 Code Output Prediction

4. Predict the output:

```dart
print("A");
Future(() => print("B"));
print("C");
```

---

5. Predict the output:

```dart
Future.delayed(Duration(seconds: 1), (){
  print("Loaded");
});
print("Start");
```

---

6. What will happen here? Will it wait or not?

```dart
Future<String> getName() {
  return Future.delayed(Duration(seconds: 2), () => "Alex");
}

void main(){
  print(getName());
}
```

---

### 🛠 Coding Tasks

7. Create a Future called `fetchWeather()` that returns `"Sunny"` after 2 seconds.

8. Write a program using **async + await** that prints:

```
Start
Fetching Data...
Data Loaded!
End
```

---

9. Create a Future `getMarks()` that returns 88 after 3 seconds and print it.

---

10. Write a Future function with **then()** instead of await:

```
Output:
Reading File...
File Read Complete!
```

---

11. Create a function `processPayment()`
    → wait 4 seconds
    → then print `"Payment Successful"`.

---

### 🔥 Slight Advanced

12. Write a Future with **try/catch** that throws `"Server Error"`.

---

13. Run two Futures simultaneously using **Future.wait()**:

```
Task1 → completes in 1 second
Task2 → completes in 2 seconds
Print final list of results
```

---

14. Convert the following `.then()` code to `async / await`:

```dart
getUser().then((value) => print(value));
```

---

15. Write a Future chain using:

```
.then()
.catchError()
.whenComplete()
```

Output format:

```
Data received
Error (if any)
Process Finished
```

---

