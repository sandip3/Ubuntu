# 🛠️ Utilities

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 4. Installing Utilities 🛠️

---

### 🔥 Firewall Configuration

* Install **Firewall Configuration** from Ubuntu Software

---

### 📸 Install Cheese

⚪ Universal

```bash id="e3y9mh"
sudo apt install cheese -y
```

---

### 🎵 Rhythmbox Audio Player

🟢 LTS

```bash id="e3x8hb"
sudo add-apt-repository ppa:ubuntuhandbook1/apps -y
sudo apt-get update
sudo apt-get install rhythmbox -y
```

---

### 🎥 Install Ubuntu Restricted Extras (Media Codecs)

⚪ Universal

```bash id="q6qk49"
sudo apt install ubuntu-restricted-extras -y
```

---

### 💽 Install NTFS Support Tools

⚪ Universal

```bash id="tfplnd"
sudo apt install ntfs-3g -y
```

* Enables **read/write support** for NTFS drives

---

### 🚀 Install Preload

⚪ Universal

```bash id="6c9d04"
sudo apt install preload -y
```

---

### 👇 Minimize to Click

⚪ Universal

```bash id="o9dc4o"
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

---

### 🛠️ System Optimization with Stacer

#### Install Stacer

🟢 LTS

```bash id="zq5y2i"
sudo add-apt-repository ppa:oguzhaninan/stacer -y
sudo apt update -y
sudo apt install stacer -y
```

---

#### Launch Stacer

⚪ Universal

```bash id="3l4e9p"
stacer
```

---

### 📱 Install scrcpy

⚪ Universal

```bash id="g2u5o7"
sudo apt install scrcpy
```

---

## 5. File Sorting 📂

⚪ Universal

```bash id="b8dzmr"
gsettings set org.gnome.nautilus.preferences default-sort-order 'type'
```

---

## 💡 Notes

* Prefer **Flatpak/Snap** for isolation when possible
* Avoid unnecessary PPAs unless required

---

> ⬅️ Previous: [Setup](./setup.md) | ➡️ Next: [System Maintenance](../system/maintenance.md)
