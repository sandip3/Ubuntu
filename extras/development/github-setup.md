# 🔗 Git & GitHub Setup

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 15. Install Git 📦

⚪ Universal

```bash id="h4p2k8"
sudo apt update
sudo apt install git -y
```

---

## 16. Configure Git 🧾

⚪ Universal

```bash id="t6m3q9"
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Verify:

⚪ Universal

```bash id="z8x1c5"
git config --list
```

---

## 17. Setup SSH Key 🔐

⚪ Universal

```bash id="p7n2d4"
ssh-keygen -t ed25519 -C "your-email@example.com"
```

---

### Start SSH Agent

⚪ Universal

```bash id="k9v4m1"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

---

### Copy Public Key

⚪ Universal

```bash id="m3x8q2"
cat ~/.ssh/id_ed25519.pub
```

👉 Add this key to your GitHub account:

* GitHub → Settings → SSH Keys → New Key

---

## 18. Test Connection ✅

⚪ Universal

```bash id="d5t7r3"
ssh -T git@github.com
```

---

## 💡 Notes

* Use SSH instead of HTTPS for GitHub
* Keep your private key secure
* SSH avoids repeated login prompts

---

> ⬅️ Previous: [Shortcuts](../customization/shortcuts.md) | ➡️ Next: [Python / OpenCV](./python-opencv.md)
