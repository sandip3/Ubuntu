# 🌐 WiFi Blocking & Access Control

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 26. WiFi Website Blocking 🚫

> Configure your router to block specific websites across your network.

---

## ⚠️ Important Note

* Router interfaces differ by model
* Steps may vary slightly depending on firmware
* Works on most routers (TP-Link, etc.)

---

## 🔧 Router Access

1. Open browser
2. Go to:

```text
http://192.168.0.1/
```

3. Login using your router credentials

---

## ⚙️ Access Control Setup

1. Go to **Access Control → Setup Wizard**

Set:

* Mode: `IP Address`
* Host Description: `Custom Name`
* IP Range: `192.168.0.2 – 192.168.0.254`

---

## 🌍 Domain Blocking

1. Set Mode: `Domain Name`
2. Add websites:

```text
example.com
mangakakalot.com
mangahub.io
```

---

## ⏱️ Schedule Setup

* Select: **Everyday**
* Time: **24 Hours**

---

## 🚫 Enable Blocking

1. Enable **Internet Access Control**
2. Set policy:

```text
Deny specified domains
```

3. Save configuration

---

## 💡 Notes

* Changes apply to all devices on network
* Useful for productivity and focus
* Can be reversed anytime from router settings

---

> ⬅️ Previous: [Disk Errors](../troubleshooting/disk-errors.md) | 🏠 Back to [Extras Index](../index.md)
