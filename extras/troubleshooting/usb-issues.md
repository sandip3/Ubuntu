# 🔌 USB Issues & Detection Problems

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* ⚪ Universal

---

## 29. USB Not Detected ❌

---

## 🧠 Causes

* USB autosuspend
* Power issues
* Driver issues
* Hardware fault

---

## 🛠️ Fix 1: Check Device

⚪ Universal

```bash
lsusb
```

---

## 🛠️ Fix 2: Check Kernel Logs

⚪ Universal

```bash
dmesg | tail
```

---

## 🛠️ Fix 3: Disable USB Autosuspend

⚪ Universal

```bash
sudo nano /etc/default/tlp
```

Add:

```text
USB_AUTOSUSPEND=0
```

Apply:

⚪ Universal

```bash
sudo systemctl restart tlp
```

---

## 🛠️ Fix 4: Reload USB Drivers

⚪ Universal

```bash
sudo modprobe -r usb_storage
sudo modprobe usb_storage
```

---

## 🛠️ Fix 5: Power Reset

* Unplug USB
* Shutdown system
* Hold power button for 10 seconds
* Restart

---

## 💡 Notes

* USB autosuspend is common cause
* Hardware ports can fail
* Always test with another port/device

---

> ⬅️ Previous: [Mount Errors](./mount-errors.md) | 🏠 Back to [Extras Index](../index.md)
