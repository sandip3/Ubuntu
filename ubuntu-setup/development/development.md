# 💻 Development Setup ⚙️

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 14. Node.js / React / Angular ⚡

### Install Node.js & npm

⚪ Universal

```bash id="s3c6f1"
sudo apt install nodejs npm
# OR (better)
nvm install node
```

---

### Verify Installation

⚪ Universal

```bash id="9m2k1d"
node -v
npm -v
```

---

### Create React App

⚪ Universal

```bash id="7n4p2e"
npx create-react-app my-app
```

---

## 15. Android Studio 📱

### Install Java (Required)

⚪ Universal

```bash id="h4x7m2"
sudo apt install openjdk-18-jdk -y
```

---

### Download Android Studio

⚪ Universal

```bash id="6v3q8p"
wget https://redirector.gvt1.com/edgedl/android/studio/ide-zips/latest/android-studio-linux.tar.gz
tar -xvf android-studio-linux.tar.gz
cd android-studio/bin
./studio.sh
```

---

## 16. Anaconda 🐍

⚪ Universal

```bash id="z8d1s6"
wget https://repo.anaconda.com/archive/Anaconda3-latest-Linux-x86_64.sh
bash Anaconda3-latest-Linux-x86_64.sh
```

---

## 17. PyCharm 🧠

⚪ Universal

```bash id="v6b2k4"
sudo snap install pycharm-community --classic
```

---

## 18. TensorFlow 🤖

⚪ Universal

```bash id="q9l5c8"
pip install tensorflow --break-system-packages
```

---

## 💡 Notes

* Keep development tools separate from general applications
* Use virtual environments (`venv`) for Python projects
* Prefer latest Node via version managers (optional future upgrade)

---

> ⬅️ Previous: [Applications](../apps/applications.md) | ➡️ Next: [Cleaning & Updates](../maintenance/cleaning.md)
