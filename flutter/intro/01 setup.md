
# 🚀 **Flutter & Dart Setup on Ubuntu – Smart Notes**

---

## 🏁 1. System Requirements

| Requirement  | Minimum                        |
| ------------ | ------------------------------ |
| OS           | Ubuntu 20.04 or later          |
| Disk Space   | 5–10 GB (recommended)          |
| Tools Needed | `git`, `curl`, `unzip`, `bash` |

---

## 📥 2. Install Required Dependencies

```bash
sudo apt-get update
sudo apt-get install git curl unzip xz-utils zip libglu1-mesa -y
```

---

## 📦 3. Download Flutter SDK Manually

```bash
cd ~/Downloads
curl -o flutter_linux.tar.xz https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_*.tar.xz
```

> *(You may choose stable/beta/dev channel depending on your need)*

---

## 📤 4. Extract Flutter & Move to System Path

```bash
tar xf flutter_linux.tar.xz
sudo mv flutter /opt/flutter
```

---

## 🔗 5. Add Flutter to PATH

```bash
echo 'export PATH="/opt/flutter/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

Check installation:

```bash
flutter --version
```

---

## ⚡ 6. Enable Android/Linux Development

### 📌 Install Android Studio (Optional for mobile build)

```bash
sudo snap install android-studio --classic
```

> After opening Android Studio → Install **SDK, Platform Tools & Emulator**

Then:

```bash
flutter doctor --android-licenses
```

---

### 🖥 Linux Desktop Build

```bash
sudo apt-get install clang cmake ninja-build pkg-config libgtk-3-dev -y
flutter config --enable-linux-desktop
```

---

## 📱 Enable Chrome Web App Support

```bash
flutter config --enable-web
sudo apt-get install chromium-browser -y
```

---

## 🧪 Verify Setup

```bash
flutter doctor
```

✔ Fix issues shown
✔ Make sure device target is detected

---

## 🧵 Optional: Install Dart Separately

Flutter bundles Dart already.
But to install Dart standalone:

```bash
sudo apt-get update
sudo apt-get install apt-transport-https
sudo sh -c 'wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -'
sudo sh -c 'wget -qO /etc/apt/sources.list.d/dart_stable.list https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list'
sudo apt-get update
sudo apt-get install dart
```

Check Dart:

```bash
dart --version
```

---

# 🔥 Quick Summary (Perfect for Revision)

| Step                 | Command                                    |
| -------------------- | ------------------------------------------ |
| Install dependencies | `sudo apt install git curl unzip xz-utils` |
| Download Flutter SDK | `curl -o flutter_linux.tar.xz <url>`       |
| Extract              | `tar xf flutter_linux.tar.xz`              |
| Add PATH             | `export PATH="/opt/flutter/bin:$PATH"`     |
| Verify               | `flutter doctor`                           |

