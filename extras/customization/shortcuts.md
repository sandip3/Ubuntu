# ⌨️ Shortcuts & Automation

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 11. Keyboard Shortcuts ⌨️

Open **Settings → Keyboard → Keyboard Shortcuts**

---

### 🚪 Close Window

* Shortcut: `Super + Shift + C`

---

### 🔥 Firefox Developer Edition

* Name: Firefox Developer Edition
* Shortcut: `Super + D`
* Command:

```bash id="c1k8v2"
firefox-developer
```

---

### 🌐 Tor Browser

* Name: Tor Browser
* Shortcut: `Super + T`
* Command:

```bash id="r5m2p7"
sh -c '"/home/$USER/Downloads/tor-browser/Browser/start-tor-browser" --detach'
```

---

### 🦊 Firefox

* Name: Firefox
* Shortcut: `Super + B`
* Command:

```bash id="v2n9q4"
firefox
```

---

### 📂 File Manager

* Name: File Manager
* Shortcut: `Super + F`
* Command:

```bash id="z8d1k3"
nautilus
```

---

### 🖥️ Terminal

* Name: Terminal
* Shortcut: `Super + Enter`
* Command:

```bash id="p4r7x1"
gnome-terminal
```

---

## 12. Startup Applications 🚀

Use **Startup Applications** or **GNOME Tweaks**

---

### ⏳ Delay Startup

⚪ Universal

```bash id="n6k3d2"
sleep 30; <app_name>
```

---

### 🔄 Run in Background

⚪ Universal

```bash id="q7p9v5"
<app_name> --background
```

---

## 13. Auto-Mount External Drive 💽

⚪ Universal

```bash id="h2t8m4"
sudo gnome-disks
```

Steps:

* Select disk
* Click ⚙️ → Edit Mount Options
* Disable “User Session Defaults”
* Enable auto-mount

---

## 14. Auto Wallpaper Change 🌄

⚪ Universal

```bash id="g5x2c8"
sudo add-apt-repository ppa:peterlevi/ppa -y
sudo apt update
sudo apt install variety -y
```

---

## 💡 Notes

* Use shortcuts to improve workflow speed
* Startup apps help automate daily tasks
* Delay heavy apps to reduce boot lag

---

> ⬅️ Previous: [Zsh Setup](./zsh.md) | ➡️ Next: [Development Tools](../development/github-setup.md)
