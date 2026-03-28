# 🌐 Browsers

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 11. Firefox Setup 🦊

### Install Firefox (Manual Latest Version)

⚪ Universal

```bash
wget https://download.mozilla.org/?product=firefox-latest&os=linux64&lang=en-US -O firefox.tar.bz2
tar xjf firefox.tar.bz2
sudo mv firefox /opt/firefox
sudo ln -s /opt/firefox/firefox /usr/local/bin/firefox
```
⚠️ Manual install will not auto-update via apt

---

### Firefox Developer Edition

⚪ Universal

```bash
wget https://download.mozilla.org/?product=firefox-devedition-latest&os=linux64&lang=en-US -O firefox-dev.tar.bz2
tar xjf firefox-dev.tar.bz2
sudo mv firefox /opt/firefox-dev
sudo ln -s /opt/firefox-dev/firefox /usr/local/bin/firefox-dev
```

---

## 12. SQLite Browser 🗄️

⚪ Universal

```bash
sudo apt install sqlitebrowser -y
```

---

## 💡 Notes

* Manual Firefox install gives **latest version**, independent of Ubuntu repos
* Use Developer Edition for web development
* SQLite Browser useful for database inspection

---

> ⬅️ Previous: [Hardware & Connectivity](../system/hardware.md) | ➡️ Next: [Applications](./applications.md)
