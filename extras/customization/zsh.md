# 🐚 Zsh Setup & Customization

---

## 🔙 Back to Extras

👉 [Go to Extras Index](../index.md)

---

### 🏷️ Command Compatibility

* 🟢 LTS → Stable for Ubuntu LTS (22.04, 24.04)
* 🔵 Non-LTS → For newer Ubuntu releases (23.x, 25.x)
* ⚪ Universal → Works on all versions

---

## 4. Install Zsh 🖥️

⚪ Universal

```bash id="z1x7c9"
sudo apt update
sudo apt install zsh git fonts-font-awesome -y
```

---

## 5. Set Zsh as Default Shell 🔄

⚪ Universal

```bash id="c9v2k3"
chsh
```

Enter:

```text id="l7q1m5"
/bin/zsh
```

---

## 6. Install Oh My Zsh ✨

⚪ Universal

```bash id="o2k8n4"
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

---

## 7. Enable Plugins 🔌

⚪ Universal

```bash id="x4m6t1"
nano ~/.zshrc
```

Add:

```bash id="v9j3s7"
plugins=(git)
```

---

### ➕ Add Auto-suggestions

⚪ Universal

```bash id="k2p5d8"
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

---

### ➕ Add Syntax Highlighting

⚪ Universal

```bash id="r6t1b4"
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Update plugins:

```bash id="j8y4w2"
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

---

## 8. Powerlevel10k Theme 🎨

⚪ Universal

```bash id="p5n2k8"
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Edit config:

⚪ Universal

```bash id="u7m9c3"
nano ~/.zshrc
```

Set:

```bash id="d4k1n6"
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Apply:

⚪ Universal

```bash id="e6v8q2"
zsh
```

---

## 9. Enable Auto-completion ⌨️

⚪ Universal

```bash id="a3w7s5"
nano ~/.zshrc
```

Add:

```bash id="b2x9t4"
autoload -U compinit
zstyle ':completion:*' menu select
zmodload zsh/complist
setopt extendedglob
_comp_options+=(globdots)
```

---

## 10. Improve History 🕒

⚪ Universal

```bash id="m1p8c7"
nano ~/.zshrc
```

Add:

```bash id="n4q6r2"
HISTSIZE=10000
SAVEHIST=10000
setopt appendhistory
setopt INC_APPEND_HISTORY
setopt SHARE_HISTORY
```

---

## 💡 Notes

* Zsh + Oh My Zsh improves productivity significantly
* Powerlevel10k provides advanced UI customization
* Plugins enhance usability (auto-suggest, highlighting)

---

> ⬅️ Previous: [Themes](./themes.md) | ➡️ Next: [Shortcuts](./shortcuts.md)
