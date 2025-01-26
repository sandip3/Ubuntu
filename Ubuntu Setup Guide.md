# 📚 Ultimate Ubuntu Setup Guide 📚

**Index:**

1. [Customizing the Boot Manager](#0-customizing-the-boot-manager-🖥️) 🖥️
2. [Setting Up a New "Dub" File](#1-setting-up-a-new-dub-file-📁) 📁
3. [Package Managers](#2-package-managers-📦) 📦
   - [Synaptic Package Manager](#synaptic-package-manager-🖥️‍🔍) 🖥️‍🔍
   - [Flatpak](#flatpak-📦) 📦
4. [Basic](#3-basic-⚙️) ⚙️
   - [Fully Charged Notification](#fully-charged-notification-🔋) 🔋
   - [Low Battery Notification](#low-battery-notification-🔋) 🔋
   - [Gnome Shell Integration](#gnome-shell-integration-🐚) 🐚
5. [Installing Utilities](#4-installing-utilities-🛠️) 🛠️
   - [Install Cheese](#install-cheese)
   - [Install Ubuntu Restricted Extras](#install-ubuntu-restricted-extras-media-codecs-🎥) 🎥
   - [Install Preload](#install-preload-🚀) 🚀
   - [Minimize to Click](#minimize-to-click-👇) 👇
   - [System Optimization with Stacer](#system-optimization-with-stacer-🛠️) 🛠️
   - [Install scrcpy](#install-scrcpy-📱) 📱
6. [File Sorting](#5-file-sorting-📂) 📂
7. [System Maintenance](#6-system-maintenance-cleaning-🧹) 🧹
8. [Improve Laptop Battery](#7-improve-laptop-battery-🔋) 🔋
9. [Enable/Disable Bluetooth on Startup](#8-enabledisable-bluetooth-on-startup-🎧) 🎧
10. [Enable/Disable Wi-Fi on Startup](#9-enabledisable-wi-fi-on-startup-📡) 📡
11. [Browsers](#10-browsers-🌐) 🌐
    - [Firefox Setup](#firefox-setup-🦊) 🦊
    - [Firefox Developer Edition](#firefox-developer-edition-🦊) 🦊
    - [SQL lite Browser](#installing-and-using-sqlite-browser-on-ubuntu-📊)📊
12. [Cleaning Tools](#11-cleaning-tools-🧼) 🧼
    - [BleachBit](#bleachbit-🧽) 🧽
13. [Update & Upgrade](#12-update--upgrade-🔄) 🔄
14. [Installing Applications](#13-installing-applications-📦) 📦
    - [Installing LibreOffice on Ubuntu](#installing-libreoffice-on-ubuntu-📊) 📊
    - [Email Client: Mozilla Thunderbird](#email-client-mozilla-thunderbird-📧) 📧
    - [Calendar: GNOME Calendar](#calendar-gnome-calendar-🗓️) 🗓️
    - [installing Spotify on Ubuntu](#installing-spotify-on-ubuntu-🎵)🎵
    - [Android Studio Setup](#android-studio-setup-📱) 📱
    - [Install obsidian ( flatpak )](#install-obsidian-using-flatpak-🌌) 🌌
    - [Tor Browser](#tor-browser-🔒) 🔒
    - [Favorite Apps (VLC, GIMP, GNOME Partition Editor)](#favorite-apps-vlc-gimp-gnome-partition-editor-🖼️) 🖼️
    - [Anaconda Setup](#anaconda-setup-⚙️)⚙️
    - [Thonny](#thonny-installation-🐍)🐍
    - [PyCharm Community Edition](#pycharm-community-edition-🐍🌄)
    - [Node.js and Angular Setup](#nodejs--react-and-angular-setup-⚙️) ⚙️
    - [Installing TensorFlow on Ubuntu](#installing-tensorflow-on-ubuntu-🧠) 🧠
15. [Uninstalling Applications](#14-uninstalling-applications) 📦
    - [Uninstalling LibreOffice ](#uninstalling-libreoffice-🗑️)🗑️
    - [Uninstalling Node.js](#uninstalling-nodejs-⚙️) ⚙️
    - [Uninstalling Android Studio](#uninstalling-android-studio-📱) 📱
    - [Uninstalling PyCharm Community Edition](#uninstalling-pycharm-community-edition-🐍) 🐍

---

## 0. Customizing the Boot Manager 🖥️

### Installing `rEFInd` Boot Manager
```bash
sudo apt install refind
reboot
```

### Configuring rEFInd Boot Manager
- Set rEFInd's boot priority in BIOS to the top.
- Restart the system.
- Hide unnecessary partitions by pressing `delete` and confirming with `yes`.
- Press `esc` to refresh.
- Restart Ubuntu again.

### Installing and Customizing rEFInd Theme (Glassy)
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

#### Editing rEFInd Configuration
```bash
cd /mnt/EFI/refind
nano refind.conf 
```
- Add `include themes/rEFInd-glassy/theme.conf` at the bottom.
- Save and reboot to see the changes.


---

## 1. Setting Up a New "Dub" File 📁
Right-click the file and open with "Software Installer". Click the "Install" button.

## 2. Package Managers 📦

### Synaptic Package Manager 🖥️‍🔍
```bash
sudo apt install synaptic -y
```

### Flatpak 📦
```bash
sudo add-apt-repository ppa:flatpak/stable -y
sudo apt update -y
sudo apt install flatpak -y
sudo apt install gnome-software-plugin-flatpak -y
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
- Restart the PC 
- Go to this website: https://flathub.org/

## 3. Basic ⚙️

### Fully Charged Notification 🔋
```bash
sudo apt-get install acpi -y
git clone https://github.com/hg8/battery-full-notification.git
cd battery-full-notification/
chmod +x batteryfull.sh
cp batteryfull.sh ~/bin
sudo cp batteryfull.sh /usr/local/bin
```
- Add this file to Startup Applications :
```
Name : Battery Full Notification
Command : /home/sandy/battery-full-notification/batteryfull.sh
Comment : Display a notification when battery is full
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
sudo apt install gnome-shell-extensions -y
```

## 4. Installing Utilities 🛠️

### Firewall Configuration 🔥

- Download "Firewall Configuration" from ubuntu software

### Install Cheese:

```bash
sudo apt install cheese
```

### Rhythmbox Audio Player

```bash
sudo add-apt-repository ppa:ubuntuhandbook1/apps
sudo apt-get update
sudo apt-get install rhythmbox
```

### Install Ubuntu Restricted Extras (Media Codecs) 🎥
```bash
sudo apt install ubuntu-restricted-extras -y
```

### Install Preload 🚀
```bash
sudo apt install preload -y
```

### Minimize to Click 👇
```bash
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

### System Optimization with Stacer 🛠️

#### Install Stacer 🚀

Stacer is a handy system optimizer and monitoring tool for Linux. It allows you to manage various aspects of your system and keep it running smoothly.

To install Stacer, open a terminal and run the following commands:

```bash
sudo add-apt-repository ppa:oguzhaninan/stacer -y
sudo apt update -y
sudo apt install stacer -y
```

#### Launch Stacer 🚀

You can launch Stacer by searching for it in the application menu or by running the following command in the terminal:

```bash
stacer
```

Stacer will provide you with a user-friendly interface to manage and optimize your Ubuntu system.

### Install scrcpy 📱
```bash
sudo snap install scrcpy
```

## 5. File Sorting 📂
```bash
gsettings set org.gnome.nautilus.preferences default-sort-order 'type'
```

## 6. System Maintenance [cleaning] 🧹
```bash
sudo apt autoremove -y
```

## 7. Improve Laptop Battery 🔋
```bash
sudo apt install tlp tlp-rdw -y
```
- Just run the above command, and you don’t need to do anything else. It’ll make your laptop battery last longer by implementing some power-saving protocols.

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

## 10. ## Disable/Enable AnyDesk Service on Startup 💻  
```bash
sudo systemctl disable anydesk.service
sudo systemctl status anydesk
```

**Note**: You might want to stop it first (or after) if it is running:  
```bash
sudo service anydesk stop
```

To start the AnyDesk service manually:  
```bash
sudo service anydesk start
```

## 11. Browsers 🌐

### Firefox Setup 🦊

- First Go to the **[Official Site](https://support.mozilla.org/en-US/kb/install-firefox-linux)** of Firefox and Download ".bz2" File

```bash
cd ~/Downloads
tar xjf firefox-*.tar.bz2
sudo mv firefox /opt
sudo ln -s /opt/firefox/firefox /usr/local/bin/firefox
sudo wget https://raw.githubusercontent.com/mozilla/sumo-kb/main/install-firefox-linux/firefox.desktop -P /usr/local/share/applications
```

---

### Firefox Developer Edition 🦊

- First Go to the **[Official Site](https://www.mozilla.org/en-US/firefox/developer/)** of Firefox and Download ".bz2" File
- unzip file and rename it "firefox-developer"

```bash
sudo mv firefox-developer /opt
sudo ln -s /opt/firefox-developer/firefox /usr/local/bin/firefox-developer
cd ~/Desktop
nano ~/.local/share/applications/firefox-developer-edition.desktop
```

- Add the following content to the `firefox-developer-edition.desktop` file

```bash
[Desktop Entry]
Name=Firefox Developer Edition
Comment=Web Browser
Exec=/opt/firefox-developer/firefox %u
Terminal=false
X-MultipleArgs=false
Type=Application
Icon=/opt/firefox-developer/browser/chrome/icons/default/default128.png
Categories=Network;WebBrowser;
MimeType=text/html;text/xml;application/xhtml+xml;application/xml;application/vnd.mozilla.xul+xml;application/rss+xml;application/rdf+xml;image/gif;image/jpeg;image/png;x-scheme-handler/http;x-scheme-handler/https;
StartupWMClass=Firefox Developer Edition
StartupNotify=true
```

---

### Installing and Using SQLite Browser on Ubuntu 📊

**1. Install SQLite Browser:**

Open your terminal and run:
```bash
sudo apt update
sudo apt install sqlitebrowser -y
```

**2. Launch SQLite Browser:**

After installation, you can start SQLite Browser from the terminal or application menu.

To start from the terminal, run:
```bash
sqlitebrowser
```

**3. Using SQLite Browser:**

- **Open a Database:**
  - Click on `File` > `Open Database` and select your `.db` file.

- **Create a New Database:**
  - Click on `File` > `New Database`, enter the name for your new database, and save it.

- **Execute SQL Queries:**
  - Go to the `Execute SQL` tab where you can enter and run SQL queries.

- **Example SQL Commands:**

  - **Create a Table:**
    ```sql
    CREATE TABLE mytable (
        id INTEGER PRIMARY KEY AUTOINCREMENT,
        name TEXT NOT NULL
    );
    ```

  - **Insert Data:**
    ```sql
    INSERT INTO mytable (name) VALUES ('example');
    ```

  - **Query Data:**
    ```sql
    SELECT * FROM mytable;
    ```

  - **Delete Data:**
    ```sql
    DELETE FROM mytable WHERE id = 1;
    ```

- **Save Changes:**
  - Make sure to save any changes to the database by clicking on `File` > `Save` or using the save icon.

- SQLite Browser provides a graphical interface for managing SQLite databases, making it easier to perform database operations without writing commands in the terminal.


## 12. Cleaning Tools 🧼

### BleachBit 🧽
```bash
sudo apt install bleachbit -y
```

## 13. Update & Upgrade 🔄
```bash
sudo apt update && sudo apt upgrade -y
sudo apt-get update -y
```

## 14. Installing Applications 📦

### Installing LibreOffice on Ubuntu 📊

Use the following steps to install the LibreOffice  pplication on a Ubuntu system.

 1. Add the LibreOffice PPA to the Ubuntu system:
```bash
sudo add-apt-repository ppa:libreoffice/ppa
```

2. Update the Apt cache:
```bash
sudo apt update
```

3. Install the complete LibreOffice suite on Ubuntu system:
```bash
sudo apt install libreoffice
```
- When prompted for confirmation, press ‘y’ and hit enter to continue.

---
### Email Client: Mozilla Thunderbird 📧

```bash
sudo apt install thunderbird -y
```
---
### Calendar: GNOME Calendar 🗓️

```bash
sudo apt install gnome-calendar -y
```
---

### installing Spotify on Ubuntu 🎵

1. Configure the Spotify Debian Repository:

```bash
curl -sS https://download.spotify.com/debian/pubkey_7A3A762FAFD4A51F.gpg | sudo gpg --dearmor --yes -o /etc/apt/trusted.gpg.d/spotify.gpg
echo "deb http://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
```
2. Update the Apt cache:

```bash
sudo apt-get update
```

3. Install the Spotify client:

```bash
sudo apt-get install spotify-client
```
---

### Install Figma 🖌️

To install Figma on Ubuntu, use the `figma-linux` package with `snap`. Follow the steps below:

1. **Install Figma-Linux:**
   Open your terminal and run:
   ```bash
   sudo snap install figma-linux
   ```

2. **Enable Local Fonts:**
   To use local fonts with the snapd version, create a symbolic link:
   ```bash
   sudo ln -s $HOME/.local/share/fonts $HOME/snap/figma-linux/current/.local/share/
   ```

3. **Launch Figma:**
   After installation, search for "Figma" in your applications menu or run:
   ```bash
   figma-linux
   ```

---
### Android Studio Setup 📱
```bash
sudo apt-get install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils -y
sudo apt update -y
sudo apt upgrade -y
sudo apt install openjdk-18-jdk -y
```
- https://developer.android.com/studio#downloads		
- Go to this Site and Download Android Studio latest version & unzip it 
```bash
sudo mv android-studio /opt/
sudo ln -sf /opt/android-studio/bin/studio.sh /bin/android-studio
```
- Once you have run these commands, you will write a snippet of code to allow the Android Studio application to be available on the application menu shortcut on Ubuntu. 

`sudo nano /usr/share/applications/android-studio.desktop`
- Add the following code snippet and save: 

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

### Install Obsidian using Flatpak 🌌

- To enhance your productivity and note-taking experience, you can install Obsidian using Flatpak. Follow the steps below:

1. **Install Obsidian:**
    Open your terminal and execute the following command to install Obsidian:

    ```bash
    flatpak install flathub md.obsidian.Obsidian
    ```

2. **Open Obsidian:**
    Once the installation is complete, launch Obsidian with the following command:

    ```bash
    flatpak run md.obsidian.Obsidian
    ```

- Now, Obsidian is ready to help you organize and connect your thoughts seamlessly. Enjoy your note-taking journey with Obsidian! 🚀✨

---


### Tor Browser 🔒
- Download Tor browser file
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
sudo apt install vlc gimp gparted -y
```

---

### Anaconda Setup ⚙️

- To install Anaconda on Ubuntu, follow these steps:

1. **Update System**: Open a terminal and update your system's package list:

   ```bash
   sudo apt update -y
   sudo apt install curl -y
   sudo apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6 -y
   ```

2. **Download Anaconda**: Open a terminal window and visit the [Anaconda download page](https://www.anaconda.com/products/distribution) to get the link for the latest version of Anaconda for Linux.

3. **Download using `wget`**: In the terminal, use the `wget` command to download the installer. Replace the link below with the actual link you obtained from the Anaconda website.

   ```bash
   wget https://repo.anaconda.com/archive/Anaconda3-<version>-Linux-x86_64.sh
   ```

4. **Install Anaconda**: Run the downloaded shell script to install Anaconda. Replace `<version>` with the actual version you downloaded.

   ```bash
   bash Anaconda3-<version>-Linux-x86_64.sh -y
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
   conda update --all -y
   ```

9. **Launch Anaconda Navigator**: To use the Anaconda Navigator GUI, you can launch it from the terminal:

   ```bash
   anaconda-navigator
   ```

10. [Create Anaconda Navigator Desktop Shortcut on Linux](https://linux.how2shout.com/create-anaconda-navigator-desktop-shortcut-ubuntu-20-04-18-04/)

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

### Thonny Installation 🐍
```bash
sudo apt install thonny -y
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

### Uninstalling LibreOffice 🗑️

1. Remove LibreOffice:
```bash
sudo apt remove --purge libreoffice
```

2. Auto-remove any residual dependencies:
```bash
sudo apt autoremove
```

3. Disable the LibreOffice PPA:
```bash
sudo add-apt-repository --remove ppa:libreoffice/ppa
```

---

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

---
