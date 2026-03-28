# 🗑️ Uninstalling Applications

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 21. Uninstall Applications 🗑️

---

### 🧾 Remove LibreOffice

⚪ Universal

```bash id="l2d9m4"
sudo apt remove --purge libreoffice* -y
sudo apt autoremove -y
```

---

### ⚡ Remove Node.js

⚪ Universal

```bash id="n8f3k2"
sudo apt-get purge --auto-remove nodejs -y
```

---

### 📱 Remove Android Studio

⚪ Universal

```bash id="k5v7q1"
rm -rf ~/android-studio
rm -rf ~/.android
rm -rf ~/.config/Google/AndroidStudio*
```
⚠️ Be careful — deletes app configs

---

### 🧠 Remove PyCharm

⚪ Universal

```bash id="q1p6x9"
sudo snap remove pycharm-community
```

---

## 💡 Notes

* Always double-check before removing packages
* Use `--dry-run` where possible
* Removing dev tools won’t affect system stability

---

> ⬅️ Previous: [Cleaning & Updates](./cleaning.md) | 🏠 Back to [Index](../index.md)
