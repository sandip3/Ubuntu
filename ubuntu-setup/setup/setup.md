# 🔧 Setup

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## ⚡ Quick Start (Recommended)

⚪ Universal

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install git curl build-essential -y
```

---

## 0. Customizing the Boot Manager 🖥️

### Installing `rEFInd` Boot Manager

⚪ Universal

```bash
sudo apt install refind
reboot
```

---

### Configuring rEFInd Boot Manager

* Set rEFInd boot priority in BIOS to top
* Restart system
* Hide unnecessary partitions (`delete` → `yes`)
* Press `esc` to refresh
* Restart Ubuntu

---

### Installing rEFInd Theme (Glassy)

⚪ Universal

```bash
cd Downloads/
git clone https://github.com/Pr0cella/rEFInd-glassy
sudo su
mount /dev/nvme0n1p1 /mnt     # Use your EFI partition's path
cd /mnt/EFI/refind/
mkdir themes
mv /home/saint/Downloads/rEFInd-glassy /mnt/EFI/refind/themes/   # Replace with actual path
cd themes
```

---

### Editing rEFInd Config

⚪ Universal

```bash
cd /mnt/EFI/refind
nano refind.conf
```

⚠️ Replace with your EFI partition (use `lsblk`)

- Add include `themes/rEFInd-glassy/theme.conf` at the bottom.
- Save and reboot to see the changes.


---

## 1. Setting Up a New Deb File 📁

* Right-click `.deb` file
* Open with **Software Installer**
* Click Install

---

## 2. Package Managers 📦

### Synaptic Package Manager

⚪ Universal

```bash
sudo apt install synaptic -y
```

---

### Flatpak

⚪ Universal

```bash
sudo apt update -y
sudo apt install flatpak -y
sudo apt install gnome-software-plugin-flatpak -y
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

* Restart system
* Visit: https://flathub.org

---

## 3. Basic Configuration ⚙️

---

### 🔋 Fully Charged Notification

⚪ Universal

```bash
sudo apt install acpi -y
git clone https://github.com/hg8/battery-full-notification.git
cd battery-full-notification/
chmod +x batteryfull.sh
sudo cp batteryfull.sh /usr/local/bin
```

Add to Startup Applications:

```text
Name : Battery Full Notification
Command : /usr/local/bin/batteryfull.sh
Comment : Display notification when battery is full
```

---

### 🔋 Low Battery Notification

⚪ Universal

```bash
cd /etc/UPower
sudo nano UPower.conf
```

Change:

```text
PercentageLow=50
PercentageCritical=35
```

---

### 🐚 GNOME Shell Integration

⚪ Universal

```bash
sudo apt install gnome-shell-extensions -y
```

---

> ➡️ Next: [Utilities](./utilities.md)
