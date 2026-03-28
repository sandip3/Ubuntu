# 🧹 System Maintenance

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 6. System Maintenance [cleaning] 🧹

> Configure automatic system cleanup so Ubuntu stays fast and stable.

---

### 🔄 Automatic APT Cleanup & Updates

⚪ Universal

```bash id="0f0m8s"
sudo nano /etc/apt/apt.conf.d/20auto-upgrades
```

Add:

```text id="n7q9o5"
APT::Periodic::Update-Package-Lists "1";
APT::Periodic::AutocleanInterval "7";
APT::Periodic::Unattended-Upgrade "1";
APT::Periodic::Download-Upgradeable-Packages "1";
APT::Periodic::Verbose "0";
APT::AutoRemove::RecommendsImportant "false";
APT::AutoRemove::SuggestsImportant "false";
```

---

### 🧾 Restart Logging Service

⚪ Universal

```bash id="yj6zn0"
sudo systemctl restart systemd-journald
```

---

### 🗑️ Temporary File Cleanup

⚪ Universal

```bash id="6o6g0k"
systemctl status systemd-tmpfiles-clean.timer
```

---

### ⚠️ Remove Unused Packages & Kernels

> Always preview before removing anything

⚪ Universal

```bash id="rjv6r6"
sudo apt autoremove --dry-run
```

⚪ Universal

```bash id="w3pr5w"
sudo apt autoremove --purge -y
```

---

### 💾 SSD Maintenance

⚪ Universal

```bash id="5lhx4d"
sudo systemctl enable fstrim.timer
sudo systemctl start fstrim.timer
```

---

## 6.1 Data & Device Safety 🛡️

> Prevent data corruption and hardware-related issues.

---

### 🔌 External Drive Safe Usage

---

### 📥 Install Required Tools

⚪ Universal

```bash id="r3mjbe"
sudo apt install ntfs-3g udisks2 tlp -y
```

---

### ⚡ Enable TLP

⚪ Universal

```bash id="4c2a7n"
sudo systemctl enable tlp
sudo systemctl start tlp
```

---

### 🔧 Disable USB Autosuspend (CRITICAL)

⚪ Universal

```bash id="6k9i0b"
sudo nano /etc/default/tlp
```

Add:

```text id="k4sk1l"
USB_AUTOSUSPEND=0
```

Apply:

⚪ Universal

```bash id="6v4m9z"
sudo systemctl restart tlp
```

Verify:

⚪ Universal

```bash id="g6r63h"
tlp-stat -u
```

---

### 🧠 Safe Eject Command

⚪ Universal

```bash id="e8c7zq"
nano ~/.bashrc
```

Add:

```bash id="h5e0i1"
alias safeusb='sync && udisksctl power-off -b /dev/sdb'
```

⚠️ Always replace `/dev/sdb` with correct device using `lsblk`

Apply:

⚪ Universal

```bash id="1u7xxt"
source ~/.bashrc
```

---

### 🔍 Find Your USB Device

⚪ Universal

```bash id="5i0h0r"
lsblk
```

> Replace `/dev/sdb` accordingly

---

### 🚀 Usage

⚪ Universal

```bash id="1q4g0u"
safeusb
```

---

### 💡 Notes

* Never unplug during file transfer

---

## 6.2 Backup Strategy 💾

⚪ Universal

```bash id="8f89ju"
rsync -av --progress ~/Documents /media/backup/
```

---

### 📂 Backup These

* Projects / Code
* `.config`
* `.ssh`
* Important documents

---

### 💡 Notes

* Backup before major changes
* Use external or cloud
* Run regularly

---

> ⬅️ Previous: [Utilities](../setup/utilities.md) | ➡️ Next: [Hardware & Connectivity](./hardware.md)
