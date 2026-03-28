# 💽 Mount Errors & Filesystem Issues

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* ⚪ Universal

---

## 28. Drive Not Mounting ❌

---

## 🧠 Common Causes

* Corrupted filesystem
* Unsupported filesystem
* Missing drivers
* Unsafe removal

---

## 🛠️ Fix 1: Identify Drive

⚪ Universal

```bash
lsblk
```

---

## 🛠️ Fix 2: Install Required Drivers

### NTFS Support

⚪ Universal

```bash
sudo apt install ntfs-3g -y
```

---

### exFAT Support

⚪ Universal

```bash
sudo apt install exfat-fuse exfat-utils -y
```

---

## 🛠️ Fix 3: Manual Mount

⚪ Universal

```bash
sudo mount /dev/sdX /mnt
```

---

## 🛠️ Fix 4: Check Logs

⚪ Universal

```bash
dmesg | tail
```

---

## 🛠️ Fix 5: Fix Filesystem

⚪ Universal

```bash
sudo fsck /dev/sdX
```

---

## 💡 Notes

* Always unmount safely
* NTFS more prone to issues on Linux
* exFAT better for cross-platform

---

> ⬅️ Previous: [Audio Fix](./audio-fix.md) | ➡️ Next: [USB Issues](./usb-issues.md)
