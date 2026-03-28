# 📦 Applications

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 13. Application Installation 📦

---

### 🧾 LibreOffice

🟢 LTS

```bash id="n2f9zt"
sudo add-apt-repository ppa:libreoffice/ppa -y
sudo apt update -y
sudo apt install libreoffice -y
```

---

### 📧 Thunderbird

⚪ Universal

```bash id="8h0e2l"
sudo apt install thunderbird -y
```

---

### 📅 GNOME Calendar

⚪ Universal

```bash id="9k2z7x"
sudo apt install gnome-calendar -y
```

---

### 🎧 Spotify

⚪ Universal

```bash id="p9l2a1"
curl -sS https://download.spotify.com/debian/pubkey_6224F9941A8AA6D1.gpg | sudo gpg --dearmor --yes -o /etc/apt/trusted.gpg.d/spotify.gpg
echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
sudo apt update
sudo apt install spotify-client -y
```
⚠️ Requires internet + repo trust

---

### 🎨 Figma (Linux)

⚪ Universal

```bash id="6f2k1q"
sudo snap install figma-linux
```

---

### 🧠 Obsidian

⚪ Universal

```bash id="0x4s7m"
flatpak install flathub md.obsidian.Obsidian
```

---

### 🧅 Tor Browser

⚪ Universal

```bash id="u7d3a9"
wget https://www.torproject.org/dist/torbrowser/tor-browser-linux64.tar.xz
tar -xvf tor-browser-linux64.tar.xz
cd tor-browser
./start-tor-browser.desktop --register-app
```

---

### 🎬 VLC / 🎨 GIMP / 💽 GParted

⚪ Universal

```bash id="r3j8v6"
sudo apt install vlc gimp gparted -y
```

---

### 🐍 Thonny (Python IDE)

⚪ Universal

```bash id="l9c5p2"
sudo apt install thonny -y
```

---

## 💡 Notes

* Use **Flatpak/Snap** where isolation is preferred
* Avoid unnecessary PPAs unless required
* Keep applications separate from development tools

---

> ⬅️ Previous: [Browsers](./browsers.md) | ➡️ Next: [Development Setup](../development/development.md)
