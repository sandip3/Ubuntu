# 🎤 Audio & Microphone Fix

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS
* 🔵 Non-LTS → Newer Ubuntu (PipeWire-based)
* ⚪ Universal → Works everywhere

---

## 27. Microphone Auto Volume Issue 🎤

> Mic volume automatically decreases or behaves inconsistently.

---

## 🧠 Cause

* PipeWire auto gain control
* Echo cancellation module
* Flat volume behavior

---

## 🛠️ Fix 1: Disable Flat Volume

⚪ Universal

```bash
mkdir -p ~/.config/pipewire
cp /usr/share/pipewire/pipewire.conf ~/.config/pipewire/
nano ~/.config/pipewire/pipewire.conf
```

Add:

```ini
flat-volumes = false
```

---

## 🛠️ Fix 2: Restart PipeWire

🔵 Non-LTS

```bash
systemctl --user restart pipewire pipewire-pulse
```

---

## 🛠️ Fix 3: Disable Echo Cancel

⚪ Universal

```bash
pactl list modules short | grep echo
```

If found:

```bash
pactl unload-module module-echo-cancel
```

---

## 🧪 Optional Check

⚪ Universal

```bash
pactl info | grep "Server Name"
```

---

## 💡 Notes

* Common issue in Ubuntu 22.04+
* Restart required after config changes
* Works for Discord, Meet, etc.

---

> ⬅️ Back: [Disk Errors](./disk-errors.md) | ➡️ Next: [Mount Errors](./mount-errors.md)
