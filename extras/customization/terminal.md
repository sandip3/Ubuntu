# 🖥️ Terminal Customization

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 1. Install GNOME Tweaks 🛠️

⚪ Universal

```bash
sudo apt install gnome-tweaks -y
```

---

## 2. Customize Terminal with Starship ⭐

---

### Install Starship

⚪ Universal

```bash
sh -c "$(curl -fsSL https://starship.rs/install.sh)"
```

---

### Enable Starship in Bash

⚪ Universal

```bash
nano ~/.bashrc
```

Add:

```bash
eval "$(starship init bash)"
```

---

### Create Configuration File

⚪ Universal

```bash
mkdir -p ~/.config && touch ~/.config/starship.toml
```

---

## 💡 Notes

* Starship provides a fast, customizable prompt
* Works across multiple shells
* Configuration file allows deep customization

---

> ⬅️ Back: [Extras Index](../index.md) | ➡️ Next: [Themes](./themes.md)
