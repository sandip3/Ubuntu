# Customization Guide 🎨🛠️

## Terminal Tweaks 🖥️

Enhance your terminal experience by installing the **gnome-tweaks** package:

```bash
sudo apt install gnome-tweaks
```

### Customizing Terminal with Starship ⭐

For a customized terminal prompt using **Starship**, follow these steps:

- Install the necessary tools:

```bash
sh -c "$(curl -fsSL https://starship.rs/install.sh)"
```

- Open your **.bashrc** file:

```bash
gedit ~/.bashrc
```

- Add the following line at the end of the file:

```bash
eval "$(starship init bash)"
```

- Create a Starship configuration file:

```bash
mkdir -p ~/.config && touch ~/.config/starship.toml
```

## Applying the Dracula Theme 🧛

Transform your interface with the iconic **Dracula** theme. Here's how you can do it:

### 💻 gnome-terminal
🛠️ Install dependencies and apply the theme to **gnome-terminal**:

```bash
sudo apt-get install dconf-cli
git clone https://github.com/dracula/gnome-terminal
cd gnome-terminal
./install.sh
```

### 🎨 Visual Studio Code
For **Visual Studio Code**, follow the instructions [here](https://draculatheme.com/visual-studio-code).

### ✏️ Gedit
For **Gedit**, use the following commands:

```bash
wget https://raw.githubusercontent.com/dracula/gedit/master/dracula.xml
```
📂 Go to this Directory and create a folder

```bash
sudo mkdir -p /home/sandy/.local/share/gedit/styles/
sudo mv dracula.xml /home/sandy/.local/share/gedit/styles/
```

Then, open **Gedit**, go to "**Preferences > Font & Color**" and select the **Dracula** theme.

### 🎨 GTK applications
🎨 Apply the theme to GTK applications:

First, [download](https://draculatheme.com/gtk) the .zip file from their site and extract it.

```bash
cd Downloads/
sudo mv gtk-master /usr/share/themes/
gsettings set org.gnome.desktop.interface gtk-theme "Dracula"
gsettings set org.gnome.desktop.wm.preferences theme "Dracula"
```

Then, download the **Icon Theme** .zip file from their site and extract it.

```bash
cd Downloads/
sudo mv Dracula /usr/share/icons
```

🛠️ If you don't have Tweaks, install it:

```bash
sudo apt install gnome-tweaks
```

Go to Appearance > Application = "Gtk-master"
Go to Appearance > Icons = "Dracula"

### 🌌 Dracula wallpaper
🖼️ Set the Dracula wallpaper by following the steps [here](https://draculatheme.com/wallpaper).

### ⛈️ QBittorrent
For [**QBittorrent**](https://draculatheme.com/qbittorrent), download the theme and apply it through the application settings.

- First, download the .zip file from their site.
- Then, open the QBittorrent app and enable theme selection from menu: Tools -> Options -> Behavior -> Interface -> Use custom UI Theme.
- In 'UI Theme file,' click on the file icon and select your '.qbtheme' file.
- Restart QBittorrent to apply the theme.

🌟 Enjoy the dark, stylish world of Dracula theme across your applications! 🌙🧛‍♂️🦇


## Key Bindings ⌨️

Customize key bindings by following these steps:

1. Open "Keyboard Shortcuts" in the system settings.

2. Configure shortcuts for various applications:

   ### Close Window 🚪❌
   - Shortcut: (Windows key) Super + Shift + C
   - Description: Quickly close windows.

   ### Firefox Developer Edition 🔥👨‍💻
   - Name: Firefox Developer Edition
   - Shortcut: (Windows key) Super + D
   - Command: `firefox-developer`
   - Description: Open Firefox Developer Edition.

   ### Tor Browser 🌐🌌
   - Name: Tor Browser
   - Shortcut: (Windows key) Super + T
   - Command:
     ```bash
     sh -c '"/home/sandy/Downloads/tor-browser-linux64-12.0.1_ALL/tor-browser/Browser/start-tor-browser" --detach || ([ !  -x "/home/sandy/Downloads/tor-browser-linux64-12.0.1_ALL/tor-browser/Browser/start-tor-browser" ] && "$(dirname "$*")"/Browser/start-tor-browser --detach)' dummy %k
     ```
   - Description: Launch Tor Browser.

   ### Firefox 🦊🌍
   - Name: Firefox
   - Shortcut: (Windows key) Super + B
   - Command: `firefox`
   - Description: Open Mozilla Firefox.

   ### File Manager 📂🗄️
   - Name: File Manager
   - Shortcut: (Windows key) Super + F
   - Command: `nautilus`
   - Description: Open the file manager.

   ### Terminal 🖥️🔍
   - Name: Terminal
   - Shortcut: (Windows key) Super + Enter
   - Command: `gnome-terminal`
   - Description: Open the terminal.

## Zsh Setup 🖥️

Follow these steps to set up **Zsh**:

```bash
sudo apt update
sudo apt install zsh git fonts-font-awesome
zsh
(then, press option 0)
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
(then, press 'n')
```

### Enable Plugins 🔌

To enable plugins in Oh My Zsh, follow these steps:

```bash
cd ~/.oh-my-zsh/plugins
ls
```

## Enable Auto-suggestions 🤖

To enable auto-suggestions, execute this command:

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

## Enable Syntax Highlighting 🌈

To enable syntax highlighting, use this command:

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
nano ~/.zshrc
(add this in plugins)
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

## Customize with Powerlevel10k Theme 🎨

To customize with the Powerlevel10k theme, follow these steps:

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
nano ~/.zshrc
ZSH_THEME="powerlevel10k/powerlevel10k"
zsh
(Once you answer all the questions, it will get you into prompt style selections where you have to choose how you want your terminal to look like)
(go with this Verbose option)
(press Y)
(you can reconfigure using this command: "p10k configure")
```

## Change Default Shell to Zsh on Ubuntu 🔄

To change your default login shell, execute the following command:

```bash
chsh
```

And to change your default shell, enter the following path of Zsh and press enter:

```bash
/bin/zsh
```

## Auto-completion Options ⌨️

Open your ".zshrc" file and add the following lines at the end

of the file:

```bash
# Basic auto/tab complete
autoload -U compinit
zstyle ':completion:*' menu select
zmodload zsh/complist
setopt extendedglob
_comp_options+=(globdots)
```

## Use History 🕒

Open your ".zshrc" file and add the following lines at the end of the file:

```bash
# For History
HISTSIZE=10000
SAVEHIST=10000
setopt appendhistory
setopt INC_APPEND_HISTORY
setopt SHARE_HISTORY
```

## Zsh Dracula Theme 🧛‍♂️

To apply the Zsh Dracula theme, follow these steps:

```bash
git clone https://github.com/dracula/zsh.git
ln -s dracula.zsh-theme/dracula.zsh-theme .oh-my-zsh/themes/dracula.zsh-theme
```

## Startup Applications 🚀

Configure startup applications using the **Startup Application** settings or through **Tweaks**.

To delay the startup of an app:

1. Click "App" -> you want to Delay at startup
2. Click "Edit" for the desired app.
3. Add the following command:

```bash
sleep 30;]"<App_Name>"
```
- This app will sleep for 10 seconds.

To launch an app in the background:

1. Click "Edit" for the desired app.
2. Use the following command:

```bash
"<App>"-background
```
- This app will start in the background.

Mount a New Hard-disk:

```bash
sudo gnome-disks
```

- Select the disk you want to start with startup.
- Click Settings, then click Edit Mount Options.
- Uncheck "User Session Defaults" if it's checked.

## Automatically Change Wallpaper with Variety 🌄

🖼️ Install **Variety** to automatically change wallpapers:

```bash
sudo add-apt-repository ppa:peterlevi/ppa
sudo apt-get update
sudo apt-get install variety
```
