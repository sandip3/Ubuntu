# 📚 Ultimate Ubuntu Setup Guide 📚

**Index:**

1. [Setting Up a New "Dub" File](#setting-up-a-new-dub-file) 📁
2. [Zsh Setup](#zsh-setup) 🖥️
3. [Enable Plugins](#enable-plugins) 🔌
4. [Enable Auto-suggestions](#enable-auto-suggestions) 🤖
5. [Enable Syntax Highlighting](#enable-syntax-highlighting) 🌈
6. [Customize with Powerlevel10k Theme](#customize-with-powerlevel10k-theme) 🎨
7. [Change Default Shell to Zsh on Ubuntu](#change-default-shell-to-zsh-on-ubuntu) 🔄
8. [Auto-completion Options](#auto-completion-options) ⌨️
9. [Use History](#use-history) 🕒
10. [Zsh Dracula Theme](#zsh-dracula-theme) 🧛‍♂️
11. [Package Managers](#package-managers) 📦
    - [Synaptic Package Manager](#synaptic-package-manager) 🖥️‍🔍
    - [Flatpak](#flatpak) 📦
12. [Basic](#basic) ⚙️
    - [Fully Charged Notification](#fully-charged-notification) 🔋
    - [Low Battery Notification](#low-battery-notification) 🔋
    - [Gnome Shell Integration](#gnome-shell-integration) 🐚
13. [Installing Utilities](#installing-utilities) 🛠️
    - [Install Ubuntu Restricted Extras](#install-ubuntu-restricted-extras-media-codecs) 🎥
    - [Install Preload](#install-preload) 🚀
    - [Minimize to Click](#minimize-to-click) 👇
14. [File Sorting](#file-sorting) 📂
15. [System Maintenance](#system-maintenance) 🧹
16. [Improve Laptop Battery](#improve-laptop-battery) 🔋
17. [Enable/Disable Bluetooth on Startup](#enable-disable-bluetooth-on-startup) 🎧
18. [Enable/Disable Wi-Fi on Startup](#enable-disable-wi-fi-on-startup) 📡
19. [Alarm Clock](#alarm-clock) ⏰
20. [Browsers](#browsers) 🌐
    - [Firefox Setup](#firefox-setup) 🦊
    - [Firefox Developer Edition](#firefox-developer-edition) 🦊
21. [Cleaning Tools](#cleaning-tools) 🧼
    - [BleachBit](#bleachbit) 🧽
22. [Update & Upgrade](#update-upgrade) 🔄
23. [Installing Applications](#installing-applications) 📦
    - [Android Studio Setup](#android-studio-setup) 📱
    - [Tor Browser](#tor-browser) 🔒
    - [Favorite Apps (VLC, GIMP, GNOME Partition Editor)](#favorite-apps-vlc-gimp-gnome-partition-editor) 🖼️
    - [AnyDesk on Ubuntu 22.04](#anydesk-on-ubuntu-2204) 💻
    - [Node.js and Angular Setup](#nodejs-and-angular-setup) ⚙️
24. [Uninstalling Applications](#uninstalling-applications) 📦
    - [Uninstall AnyDesk from Ubuntu](#uninstall-anydesk-from-ubuntu) 💻
    - [Uninstalling Node.js](#uninstalling-nodejs) ⚙️
    - [Uninstalling Android Studio](#uninstalling-android-studio) 📱
25. [End of Guide](#end-of-guide-) 📚

---

## 1. Setting Up a New "Dub" File 📁
Right-click the file and open with "Software Installer". Click the "Install" button.

## 2. Zsh Setup 🖥️
(https://itsfoss.com/zsh-ubuntu/)
```bash
sudo apt update
sudo apt install zsh git fonts-font-awesome
zsh
(then , press option 0)
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
(then , press 'n')
```

## 3. Enable Plugins 🔌
```bash
cd ~/.oh-my-zsh/plugins
ls
```
(To enable plugins in Oh My Zsh, you need to add the name of the plugin to the list of plugins in your "~/.zshrc" file.)

## 4. Enable Auto-suggestions 🤖
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

## 5. Enable Syntax Highlighting 🌈
```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
nano ~/.zshrc
(add this in plugins)
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

## 6. Customize with Powerlevel10k Theme 🎨
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
nano ~/.zshrc
ZSH_THEME="powerlevel10k/powerlevel10k"
zsh
(Once you answer all the questions, it will get you into prompt style selections where you have to choose how you want your terminal to look like)
(go with this Verbose option)
(press Y)
(you can reconfigure using this command : "p10k configure")
```

## 7. Change Default Shell to Zsh on Ubuntu 🔄
(To change your default login shell, first, execute the given command)
```bash
chsh
(And to change your default shell, enter the following path of Zsh and press enter:)
/bin/zsh
```

## 8. Auto-completion Options ⌨️
(Open ".zshrc" file and add this line's at end of file)
```bash
# Basic auto/tab complete
autoload -U compinit
zstyle ':completion:*' menu select
zmodload zsh/complist
setopt extendedglob
_comp_options+=(globdots)

```

## 9. Use History 🕒
(Open ".zshrc" file and add this line's at end of file)
```bash
# For History
HISTSIZE=10000
SAVEHIST=10000
setopt appendhistory
setopt INC_APPEND_HISTORY
setopt SHARE_HISTORY
```

## 10. Zsh Dracula Theme 🧛‍♂️
(https://draculatheme.com/zsh)
```bash
git clone https://github.com/dracula/zsh.git
ln -s dracula.zsh-theme/dracula.zsh-theme .oh-my-zsh/themes/dracula.zsh-theme
```

## 11. Package Managers 📦

### Synaptic Package Manager 🖥️‍🔍
```bash
sudo apt install synaptic
```

### Flatpak 📦
```bash
sudo add-apt-repository ppa:flatpak/stable
sudo apt update
sudo apt install flatpak
sudo apt install gnome-software-plugin-flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
- Restart the pc 
- go to this website : https://flathub.org/


## 12. Basic ⚙️

### Fully Charged Notification 🔋
```bash
sudo apt-get install acpi
git clone https://github.com/hg8/battery-full-notification.git
cd battery-full-notification/
chmod +x batteryfull.sh
cp batteryfull.sh ~/bin
sudo cp batteryfull.sh /usr/local/bin
```
- Add this file to Startup Applications :
```
Name : Battry Full Notification
Command : /home/sandy/battery-full-notification/batteryfull.sh
Comment : Display a notification when battry is full
```
---
### Low Battery Notification 🔋
```bash
cd /etc/UPower
sudo nano UPower.conf
(PercentageLow=50)
(PercentageCritical=35)
```
- Press "Ctrl + X" and save


### Gnome Shell Integration 🐚
```bash
sudo apt install gnome-shell-extensions
```

## 13. Installing Utilities 🛠️

### Install Ubuntu Restricted Extras (Media Codecs) 🎥
```bash
sudo apt install ubuntu-restricted-extras
```

### Install Preload 🚀
```bash
sudo apt install preload
```

### Minimize to Click 👇
```bash
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

## 14. File Sorting 📂
```bash
gsettings set org.gnome.nautilus.preferences default-sort-order 'type'
```

## 15. System Maintenance [cleaning] 🧹
```bash
sudo apt autoremove
```

## 16. Improve Laptop Battery 🔋
```bash
sudo apt install tlp tlp-rdw
```
- Just run the above command and you don’t need to do anything else. It’ll make your laptop battery last longer by implementing some power-saving protocols.

## 17. Enable/Disable Bluetooth on Startup 🎧
```bash
sudo systemctl disable bluetooth.service
sudo systemctl status bluetooth.service
```

```bash
sudo service bluetooth start
```

## 18. Enable/Disable Wi-Fi on Startup 📡
```bash
nmcli radio wifi on
nmcli radio wifi off
```

## 20. Browsers 🌐

### Firefox Setup 🦊
- https://support.mozilla.org/en-US/kb/install-firefox-linux

- Frist Go to Offical Site of Firefox and Download ".bz2" File
- 
```bash
cd ~/Downloads
tar xjf firefox-*.tar.bz2
sudo mv firefox /opt
sudo ln -s /opt/firefox/firefox /usr/local/bin/firefox
sudo wget https://raw.githubusercontent.com/mozilla/sumo-kb/main/install-firefox-linux/firefox.desktop -P /usr/local/share/applications
```

### Firefox Developer Edition 🦊
```bash
snap install ubuntu-make --classic
umake web firefox-dev
```

## 21. Cleaning Tools 🧼

### BleachBit 🧽
```bash
sudo apt install bleachbit
```

## 22. Update & Upgrade 🔄
```bash
sudo apt update && sudo apt upgrade
sudo apt-get update
```

## 23. Installing Applications 📦

### Android Studio Setup 📱
```bash
sudo apt-get install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils
sudo apt update
sudo apt upgrade
sudo apt install openjdk-18-jdk
```
- https://developer.android.com/studio#downloads		
- goto this Site and Download Android Studio leteset version & unzip it 
```bash
sudo mv android-studio /opt/
sudo ln -sf /opt/android-studio/bin/studio.sh /bin/android-studio
```
- Once you have run these commands, you will write a snippet of code to allow for the Android Studio application to be available on the application menu shortcut on Ubuntu. 

`sudo nano /usr/share/applications/android-studio.desktop`
-  Add the following code snippet and save: 

``` text
[Desktop Entry]
Version=1.0
Type=Application
Name=Android Studio
Comment=Android Studio
Exec=bash -i "/opt/android-studio/bin/studio.sh" %f
Icon=/opt/android-studio/bin/studio.png
Categories=Development;IDE;
Terminal=false
StartupNotify=true
StartupWMClass=jetbrains-android-studio
Name[en_GB]=android-studio.desktop
```
---
### Tor Browser 🔒
- download Tor browser file
```bash
cd Downloads
tar -xvf tor-browser-linux64-*_en-US.tar.xz
# Now extract the downloaded file
cd tor-browser_en-US/
# Switch to extract the folder
./start-tor-browser.desktop --register-app		
# For Application launcher shortcut
cp start-tor-browser.desktop ~/Desktop			
# Copy Browser shortcut to Desktop
cd ~/Desktop						
# Switch to Desktop
gio set ~/Desktop/start-tor-browser.desktop metadata::trusted true
# Allow the system to launch the desktop shortcut
chmod a+x ~/Desktop/start-tor-browser.desktop
# Give permission to execute
```

### Favorite Apps (VLC, GIMP, GNOME Partition Editor) 🖼️
```bash
sudo apt install vlc gimp gparted
```

### Node.js , React and Angular Setup ⚙️

**Installing Node.Js :**

```bash
sudo apt update
sudo apt install nodejs npm
node --version
npm --version
```

**Installing Angular:**
```bash
npm install npm@latest -g
npm install -g @angular/cli
ng version
```

**Installing React:**

```bash

```

## 24. Uninstalling Applications

### Uninstalling Node.js ⚙️
```bash
sudo apt-get purge --auto-remove nodejs
```

### Uninstalling Android Studio 📱
```bash
sudo rm /usr/share/applications/android-studio.desktop
sudo rm -r /usr/bin/android-studio
sudo rm -rf /opt/android-studio
rm -rf ~/android-studio-2022.1.1.21-linux.tar.gz
```

## 25. End of Guide 📚

---
