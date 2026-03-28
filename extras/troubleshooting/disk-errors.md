# 💽 Disk Errors & Mount Issues

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 25. Unable to Access Location Error ❌

### 🔴 Error Example

```text
unable to access location  
wrong fs type, bad superblock, missing code page, or helper program
```

---

## 🧠 Cause

* Abrupt shutdown
* Unsafe USB removal
* Filesystem corruption (NTFS/exFAT)

---

## 🛠️ Solution 1: Fix Using Linux (Recommended)

### Identify Drive

⚪ Universal

```bash id="g6p3n2"
lsblk
```

---

### Run NTFS Fix

⚪ Universal

```bash id="x2m7d8"
sudo ntfsfix /dev/sdX
```

> Replace `/dev/sdX` with your actual partition (e.g., `/dev/sdb2`)

---

### Try Mount Again

⚪ Universal

```bash id="w4z1k9"
udisksctl mount -b /dev/sdX
```

---

## 🛠️ Solution 2: Fix Using Windows 🪟

1. Plug drive into Windows
2. Open **This PC**
3. Right-click drive → **Properties**
4. Go to **Tools tab**
5. Click **Check → Scan → Repair**

---

## ⚠️ Important Notes

* Linux fix (`ntfsfix`) is **temporary repair**
* Windows performs **full filesystem repair**
* Some corrupted files may be lost

---

## 🚫 Prevention

* Always use **safe eject**
* Avoid unplugging during transfer
* Disable USB autosuspend (see main guide)
* Avoid sudden shutdowns

---

## 💡 Pro Tip

If errors happen frequently:

* Consider using **exFAT** for external drives
* Avoid NTFS for heavy Linux usage

---

> ⬅️ Previous: [Anki Extensions](../learning/anki-extensions.md) | ➡️ Next: [Networking](../networking/wifi-block.md)
