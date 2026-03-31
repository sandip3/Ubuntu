# 🌐 Browsers

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 11. Firefox Setup 🦊

### Install Firefox (Manual Latest Version)

- First Go to the **[Official Site](https://support.mozilla.org/en-US/kb/install-firefox-linux)** 

⚪ Universal

```bash
wget https://download.mozilla.org/?product=firefox-latest&os=linux64&lang=en-US -O firefox.tar.bz2
tar xjf firefox.tar.bz2
sudo mv firefox /opt/firefox
sudo ln -s /opt/firefox/firefox /usr/local/bin/firefox
sudo wget https://raw.githubusercontent.com/mozilla/sumo-kb/main/install-firefox-linux/firefox.desktop -P /usr/local/share/applications
```
⚠️ Manual install will not auto-update via apt

---

### Firefox Developer Edition


- First Go to the **[Official Site](https://www.mozilla.org/en-US/firefox/developer/)** of Firefox and Download ".bz2" File
- unzip file and rename it `firefox-developer`

⚪ Universal

```bash
sudo mv firefox-developer /opt
sudo ln -s /opt/firefox-developer/firefox /usr/local/bin/firefox-developer
cd ~/Desktop
nano ~/.local/share/applications/firefox-developer-edition.desktop
```

- Add the following content to the `firefox-developer-edition.desktop` file

```bash
[Desktop Entry]
Name=Firefox Developer Edition
Comment=Web Browser
Exec=/opt/firefox-developer/firefox %u
Terminal=false
X-MultipleArgs=false
Type=Application
Icon=/opt/firefox-developer/browser/chrome/icons/default/default128.png
Categories=Network;WebBrowser;
MimeType=text/html;text/xml;application/xhtml+xml;application/xml;application/vnd.mozilla.xul+xml;application/rss+xml;application/rdf+xml;image/gif;image/jpeg;image/png;x-scheme-handler/http;x-scheme-handler/https;
StartupWMClass=Firefox Developer Edition
StartupNotify=true
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
