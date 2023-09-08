# 📚 Ultimate Ubuntu Setup Guide 📚

**Index:**

1. [Setting Up a New "Dub" File](#1-setting-up-a-new-dub-file-📁) 📁
2. [Package Managers](#2-package-managers-📦) 📦
   - [Synaptic Package Manager](#synaptic-package-manager-🖥️‍🔍) 🖥️‍🔍
   - [Flatpak](#flatpak-📦) 📦
3. [Basic](#3-basic-⚙️) ⚙️
   - [Fully Charged Notification](#fully-charged-notification-🔋) 🔋
   - [Low Battery Notification](#low-battery-notification-🔋) 🔋
   - [Gnome Shell Integration](#gnome-shell-integration-🐚) 🐚
4. [Installing Utilities](#4-installing-utilities-🛠️) 🛠️
   - [Install Ubuntu Restricted Extras](#install-ubuntu-restricted-extras-media-codecs-🎥) 🎥
   - [Install Preload](#install-preload-🚀) 🚀
   - [Minimize to Click](#minimize-to-click-👇) 👇
5. [File Sorting](#5-file-sorting-📂) 📂
6. [System Maintenance](#6-system-maintenance-cleaning-🧹) 🧹
7. [Improve Laptop Battery](#7-improve-laptop-battery-🔋) 🔋
8. [Enable/Disable Bluetooth on Startup](#8-enabledisable-bluetooth-on-startup-🎧) 🎧
9. [Enable/Disable Wi-Fi on Startup](#9-enabledisable-wi-fi-on-startup-📡) 📡
10. [Browsers](#10-browsers-🌐) 🌐
    - [Firefox Setup](#firefox-setup-🦊) 🦊
    - [Firefox Developer Edition](#firefox-developer-edition-🦊) 🦊
11. [Cleaning Tools](#11-cleaning-tools-🧼) 🧼
    - [BleachBit](#bleachbit-🧽) 🧽
12. [Update & Upgrade](#12-update--upgrade-🔄) 🔄
13. [Installing Applications](#23-installing-applications-📦) 📦
    - [Android Studio Setup](#android-studio-setup-📱) 📱
    - [Tor Browser](#tor-browser-🔒) 🔒
    - [Favorite Apps (VLC, GIMP, GNOME Partition Editor)](#favorite-apps-vlc-gimp-gnome-partition-editor-🖼️) 🖼️
    - [Anaconda Setup](#anaconda-setup-⚙️)⚙️
    - [Thonny](#thonny-installation-🐍)🐍
    - [PyCharm Community Edition](#pycharm-community-edition)
    - [Node.js and Angular Setup](#nodejs--react-and-angular-setup-⚙️) ⚙️
    - [Installing TensorFlow on Ubuntu](#installing-tensorflow-on-ubuntu-🧠) 🧠
14. [Uninstalling Applications](#14-uninstalling-applications) 📦
    - [Uninstalling Node.js](#uninstalling-nodejs-⚙️) ⚙️
    - [Uninstalling Android Studio](#uninstalling-android-studio-📱) 📱
    - [Uninstalling PyCharm Community Edition](#uninstalling-pycharm-community-edition-📦) 📦
15. [End of Guide](#15-end-of-guide-📚) 📚

---

## 1. Setting Up a New "Dub" File 📁
Right-click the file and open with "Software Installer". Click the "Install" button.

## 2. Package Managers 📦

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


## 3. Basic ⚙️

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

## 4. Installing Utilities 🛠️

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

## 5. File Sorting 📂
```bash
gsettings set org.gnome.nautilus.preferences default-sort-order 'type'
```

## 6. System Maintenance [cleaning] 🧹
```bash
sudo apt autoremove
```

## 7. Improve Laptop Battery 🔋
```bash
sudo apt install tlp tlp-rdw
```
- Just run the above command and you don’t need to do anything else. It’ll make your laptop battery last longer by implementing some power-saving protocols.

## 8. Enable/Disable Bluetooth on Startup 🎧
```bash
sudo systemctl disable bluetooth.service
sudo systemctl status bluetooth.service
```

```bash
sudo service bluetooth start
```

## 9. Enable/Disable Wi-Fi on Startup 📡
```bash
nmcli radio wifi on
nmcli radio wifi off
```

## 10. Browsers 🌐

### Firefox Setup 🦊
- https://support.mozilla.org/en-US/kb/install-firefox-linux

- Frist Go to Offical Site of Firefox and Download ".bz2" File

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

## 11. Cleaning Tools 🧼

### BleachBit 🧽
```bash
sudo apt install bleachbit
```

## 12. Update & Upgrade 🔄
```bash
sudo apt update && sudo apt upgrade
sudo apt-get update
```

## 13. Installing Applications 📦

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

---

### Anaconda Setup ⚙️

- To install Anaconda on Ubuntu, follow these steps:

1. **Update System**: Open a terminal and update your system's package list:

   ```bash
   sudo apt update
   sudo apt install curl
   sudo apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
   ```

2. **Download Anaconda**: Open a terminal window and visit the [Anaconda download page](https://www.anaconda.com/products/distribution) to get the link for the latest version of Anaconda for Linux.

3. **Download using `wget`**: In the terminal, use the `wget` command to download the installer. Replace the link below with the actual link you obtained from the Anaconda website.

   ```bash
   wget https://repo.anaconda.com/archive/Anaconda3-<version>-Linux-x86_64.sh
   ```

4. **Install Anaconda**: Run the downloaded shell script to install Anaconda. Replace `<version>` with the actual version you downloaded.

   ```bash
   bash Anaconda3-<version>-Linux-x86_64.sh
   ```

5. **Follow the installer prompts**: You'll see some license terms. Scroll through and press `Enter` to continue. You'll be asked to review the license terms, and then prompted to choose the installation location. Press `Enter` to install in the default location or specify a different location.

6. **Initialize Anaconda**: After installation, the installer will ask if you want to initialize Anaconda by running `conda init`. It's a good idea to say yes:

   ```bash
   source ~/.bashrc
   ```

   Alternatively, you can use `source ~/.bash_profile` if you're using the Bash shell.

7. **Test Anaconda**: You can now test if Anaconda is installed by running:

   ```bash
   conda --version
   ```

   This should display the version of conda installed.

8. **Update Anaconda**: It's a good practice to update Anaconda after installation:

   ```bash
   conda update --all
   ```

9. **Launch Anaconda Navigator**: To use the Anaconda Navigator GUI, you can launch it from the terminal:

   ```bash
   anaconda-navigator
   ```

10. [Create Anaconda Navigator Desktop Shortcut on Linux] (https://linux.how2shout.com/create-anaconda-navigator-desktop-shortcut-ubuntu-20-04-18-04/)

**Step 1**: Open the **command terminal** on your Ubuntu 20.04 LTS or any other Linux system you are using.

**Step 2**: Switch to the Desktop directory by using the command: `cd Desktop`

**Step 3**: Now create a file for the **Anaconda Desktop shortcut**, for that we are using the default nano editor of Ubuntu Linux.

``` bash
nano anaconda.desktop
```

**Step 4**: You will see a text editor, where copy-paste the following text:

```bash
[Desktop Entry]
Version=1.0
Type=Application
Name=Anaconda
Exec=/home/<username>/anaconda3/bin/anaconda-navigator
Icon=/home/<username>/anaconda3/lib/python3.8/site-packages/anaconda_navigator/app/icons/Icon1024.png
Terminal=false
```

**Step 5**: The things you have to change in the above-given text are the directories for the **Exec** and **Icon** values. If you have used the **default home** directory for the **Anaconda3** installation then just replace the **<username>** with your Ubuntu Linux **username** that you can easily find on the Command terminal given before the @. Otherwise, just replace the /home/<username> with the directory path where the folder of anaconda3 you have placed. Also, don’t forget to replace the **python version** with your system default one. Here it is **3.8** and can be different in your case.

**Step 6**: Save the file by pressing **Ctrl+X** and then **Y** followed by the **Enter** Key.

**Step 7**: Now, you will see an icon on the Desktop for Anaconda, right-click on it, and select the option “**Allow Launching**“. This will turn the gear-looking icon into the **Anaconda Navigator** one. That’s it you are done!

![Allow Launhing the Desktop Shortcut Ubuntu 20.04](https://www.how2shout.com/linux/wp-content/uploads/2020/08/Allow-Launhing-the-Desktop-Shortcut-Ubuntu.jpg)
``
![Anaconda Navigator Desktop Shortcut on Ubuntu Linux](https://www.how2shout.com/linux/wp-content/uploads/2020/08/Anaconda-Navigator-Desktop-Shortcut-on-Ubuntu-Linux.jpg)

**Trivia**: The path of the anaconda-navigator executable file.

![Anaconda Navigator Installation directory](https://www.how2shout.com/linux/wp-content/uploads/2020/08/Anaconda-Navigator-Installation-directory.jpg)

**Note:**
- Remember to replace `<version>` with the actual version of Anaconda you downloaded.
- Once Anaconda is installed, you can create and manage environments, install packages, and work with data science tools using the Anaconda Navigator GUI or the command-line interface (`conda`).

---

Absolutely, let's add even more emojis for a fun touch:

### Thonny Installation 🐍
```bash
sudo apt install thonny
```

### PyCharm Community Edition Installation and Desktop Shortcut 🐍🌄

**1. 🚀 Download PyCharm Community Edition:**
   - Open a web browser and go to the official PyCharm download page: [https://www.jetbrains.com/pycharm/download/](https://www.jetbrains.com/pycharm/download/)
   - Choose the **Community** tab and download the Linux version.

**2. 📦 Extract and Install:**
   - Open a terminal and navigate to the directory where the downloaded archive is located using the `cd` command.
   - Extract the downloaded archive (replace `pycharm-community-XXXX.X.X` with your version):

   ```bash
   tar -xvf pycharm-community-XXXX.X.X.tar.gz
   ```

   - Navigate to the extracted directory:

   ```bash
   cd pycharm-community-XXXX.X.X
   ```

   - Run PyCharm:

   ```bash
   ./bin/pycharm.sh
   ```

**3. 🛠️ Initial Setup:**
   - Follow on-screen instructions to set up PyCharm according to your preferences.

**4. 🖥️ Create a Desktop Shortcut:**
   - Open a terminal and create a `.desktop` file:

   ```bash
   nano ~/.local/share/applications/pycharm-community.desktop
   ```

   - Paste this content into the file, replacing paths and version numbers:

   ```plaintext
   [Desktop Entry]
   Name=PyCharm Community
   Comment=Python IDE
   Exec=/path/to/pycharm-community-XXXX.X.X/bin/pycharm.sh
   Icon=/path/to/pycharm-community-XXXX.X.X/bin/pycharm.png
   Terminal=false
   Type=Application
   Categories=Development;IDE;
   StartupWMClass=jetbrains-pycharm
   ```

**5. 🔗 Make the Desktop Entry Executable:**
   - Make the desktop entry file executable:

   ```bash
   chmod +x ~/.local/share/applications/pycharm-community.desktop
   ```

**6. ♻️ Refresh GNOME Shell:**
   - Refresh the GNOME Shell to make the new desktop entry visible. Log out and log back in or restart the GNOME Shell:

   ```bash
   gnome-shell --replace &
   ```

By following these steps, you'll 🚀 launch into PyCharm Community Edition and create a 🌄 desktop shortcut for easy access. Just remember to replace placeholders like `/path/to/pycharm-community-XXXX.X.X` with the actual paths and version numbers corresponding to your installation. Enjoy coding! 🎉  

---

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

### Installing TensorFlow on Ubuntu 🧠

To empower your Ubuntu system with the capabilities of TensorFlow, follow these steps:

**1. 🖥️ Open a Terminal:**

   Begin your journey by summoning the terminal on your Ubuntu system. Press `Ctrl` + `Alt` + `T` to open the gateway to the command-line world.

**2. 🌐 Create a Virtual Environment (Optional):**

   While not mandatory, creating a virtual environment is a wise move to keep your TensorFlow installation isolated. To craft one, employ the mystical powers of `virtualenv`:

   ```bash
   sudo apt install python3-venv  # Harness the power of virtualenv
   python3 -m venv tensorflow-env  # Forge a virtual environment
   source tensorflow-env/bin/activate  # Awaken the virtual guardian
   ```

   Activating the virtual environment ensures that TensorFlow and its allies are confined within this realm.

**3. 🚀 Install TensorFlow:**

   With your virtual environment standing by (or without it if you prefer), you can beckon TensorFlow into your Ubuntu realm using the trusty `pip`. For CPU aficionados:

   ```bash
   pip install tensorflow
   ```

   But if you possess a compatible NVIDIA GPU and seek the accelerated might of TensorFlow with GPU support:

   ```bash
   pip install tensorflow-gpu
   ```

   Watch as the command conjures TensorFlow and its loyal comrades, bringing their powers to your aid.

**4. ✅ Verify the Installation:**

   To ensure that TensorFlow has taken its rightful place in your domain, open a Python shell by uttering the incantation `python` in your terminal. Then, recite the following spell:

   ```python
   import tensorflow as tf
   print(tf.__version__)
   ```

   Witness as the version number of TensorFlow emerges, confirming its presence and readiness.

**5. ♻️ Deactivate Virtual Environment (Optional):**

   If you summoned a virtual environment in step 2 and your quest with TensorFlow is complete, you can bid it farewell by running:

   ```bash
   deactivate
   ```

## 14. Uninstalling Applications 🗑️

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

### Uninstalling PyCharm Community Edition 🐍

**1. 🧹 Bidding Farewell to PyCharm:**
- Open a terminal and embark on a journey to the PyCharm installation directory. This digital realm, often nestled in your home directory, can be reached using the `cd` command:

   ```bash
   cd ~/pycharm-community-XXXX.X.X
   ```

   Replace `XXXX.X.X` with the version number you had installed.

- Summon your digital broom and sweep away PyCharm's remnants:

   ```bash
   rm -r ~/pycharm-community-XXXX.X.X
   ```

**2. 🚪 Uninviting from the Desktop Fiesta:**
- If you had graciously hosted PyCharm's icon at your desktop party, it's time to kindly revoke its access:

   ```bash
   rm ~/.local/share/applications/pycharm-community.desktop
   ```

**3. 🧽 Optional: Polishing Configurations and Leftovers:**
- For those embracing a burst of digital tidiness, let's give the environment a polish by clearing out any lingering configuration files and settings. Swipe away the `~/.config/JetBrains` directory:

   ```bash
   rm -r ~/.config/JetBrains
   ```

   If you're feeling the itch for meticulousness, whisk PyCharm's personalized settings into the virtual bin by removing the `~/.PyCharmXXXX.X` directory:

   ```bash
   rm -r ~/.PyCharmXXXX.X
   ```

   Replace `XXXX.X` with the version number.

With these steps, you'll conduct a digital spring cleaning, gracefully escorting PyCharm Community Edition out of your digital abode. Make sure to save any precious projects or configurations before embarking on this enchanting uninstallation quest. 🚀👋

## 15. End of Guide 📚

---
