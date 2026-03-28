# 🎨 Themes & Appearance

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 3. Apply Dracula Theme 🧛

---

### 💻 GNOME Terminal Theme

⚪ Universal

```bash id="g9f1k2"
sudo apt install dconf-cli -y
git clone https://github.com/dracula/gnome-terminal
cd gnome-terminal
./install.sh
```

---

### 🎨 GTK Theme

1. Download Dracula GTK theme from:
   👉 https://draculatheme.com/gtk

2. Extract and move:

⚪ Universal

```bash id="y2k7q8"
cd ~/Downloads/
sudo mv gtk-master /usr/share/themes/
```

3. Apply theme:

⚪ Universal

```bash id="u8d4n3"
gsettings set org.gnome.desktop.interface gtk-theme "Dracula"
gsettings set org.gnome.desktop.wm.preferences theme "Dracula"
```

---

### 🎭 Icon Theme

⚪ Universal

```bash id="v7m3k9"
cd ~/Downloads/
sudo mv Dracula /usr/share/icons
```

---

### 🛠️ Apply via GNOME Tweaks

⚪ Universal

```bash id="n4p8t1"
gnome-tweaks
```

* Appearance → Applications → `gtk-master`
* Appearance → Icons → `Dracula`

---

### ✏️ Gedit Theme

⚪ Universal

```bash id="k2f6j0"
wget https://raw.githubusercontent.com/dracula/gedit/master/dracula.xml
sudo mkdir -p ~/.local/share/gedit/styles/
mv dracula.xml ~/.local/share/gedit/styles/
```

* Open Gedit → Preferences → Font & Color
* Select **Dracula**

---

### 🌄 Wallpaper

👉 https://draculatheme.com/wallpaper

---

### 🎵 QBittorrent Theme

* Download `.qbtheme` file from Dracula website
* Open QBittorrent → Settings → Behavior → Interface
* Enable **Custom UI Theme**
* Select downloaded file
* Restart app

---

## 💡 Notes

* Dracula provides consistent dark theme across apps
* GNOME Tweaks is required for applying themes
* Always restart apps after applying themes

---

> ⬅️ Previous: [Terminal Customization](./terminal.md) | ➡️ Next: [Zsh Setup](./zsh.md)
