# 💻 Hardware & Connectivity

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 7. Improve Laptop Battery 🔋

⚪ Universal

```bash id="8n2v2x"
sudo apt install tlp tlp-rdw -y
```

* Improves battery life using power-saving optimizations
* No further configuration required

---

## 8. Bluetooth Control 🎧

### Disable on Startup

⚪ Universal

```bash id="1x4n7g"
sudo systemctl disable bluetooth.service
sudo systemctl status bluetooth.service
```

---

### Enable Manually

⚪ Universal

```bash id="1m8y2v"
sudo systemctl start bluetooth.service
```

---

## 9. Wi-Fi Control 📡

⚪ Universal

```bash id="p7f2az"
nmcli radio wifi on
nmcli radio wifi off
```

---

## 10. AnyDesk Service Control 💻

### Disable on Startup

⚪ Universal

```bash id="g3q8f0"
sudo systemctl disable anydesk.service
sudo systemctl status anydesk.service
```

---

### Stop Service

⚪ Universal

```bash id="v4h7r2"
sudo service anydesk stop
```

---

### Start Service

⚪ Universal

```bash id="r9p5y1"
sudo service anydesk start
```

---

## 💡 Notes

* TLP improves battery significantly on laptops
* Disable unused services to save resources

---

> ⬅️ Previous: [System Maintenance](./maintenance.md) | ➡️ Next: [Browsers](../apps/browsers.md)
