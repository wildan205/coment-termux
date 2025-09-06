# Requirements
- An active internet connection
- Download and Install F-Droid
- Install Termux from F-Droid
- Install Hacker's Keyboard from Google Playstore.
- Install Nethunter Kex app available on Nethunter Store
- Enough storage space on your device
#  Install F-Droid
- Download and install F-Droid APK from the official F-Droid website.
# Install Termux
- Termux is an open-source application that provides a Linux-like environment on your Android phone. It gives you a terminal interface similar to that you would find on any other Linux distribution allowing you to execute Linux commands or even run a whole Linux distribution on your Android phone. The beauty of it all is that you do not need to root your phone to run this app.

Now, there are two ways in which you can install Termux on your phone.

- Download and Install the app from F-DROiD
- Download the APK file from GitHub
- Tip: Be sure to carefully follow the steps in each method below to avoid any issues when installing Kali Linux on your Android phone later. Following the instructions closely will help prevent errors during the installation process.

- Install Termux from F-DROID
- Now that you already have F-DROID installed, launch the app from the applications menu and tap the search icon to reveal the search bar. Type the word “Termux.”
- F-droid will filter all the applications in its database and list all Termux applications and plugins available. Now select the app with the name “Termux Terminal emulator with packages.” See the image below.
- That will open a new screen where you will see more information about the app and also the “INSTALL” option.
# IMPORTANT NOTE:
- Do not tap the “INSTALL” option to start installing the app. Instead, scroll to the bottom of the app and tap “Versions.” This will reveal all the Termux versions available for installation. As of writing this post, the available versions include 0.118, 0.117, and 0.116.
- Install version 0.117. We tried working with version 0.118 (latest) and we faced so many errors when trying to launch Kali on our Android phone
- After a successful installation, you will see the “UPDATE” option. Do not update the app. Just launch Termux from the applications menu and continue using the installed version 0.117
# Install Termux from GitHub
- Another option you can use to install Termux on your phone is downloading the APK file directly from their official GitHub page. Now, unlike in F-droid where we insisted on installing Termux version 0.117, the only available version on Android is 0.118.

- Tip: From our experience, the Termux version 0.118 available on GitHub is different from version 0.118 available on F-droid. That’s because when we installed version 0.118 from F-droid we encountered so many issues and we couldn’t get Kali Linux starting on Android. However, the 0.118 version available on GitHub worked smoothly.

- On the Termux Github page, you will see a list of all available releases. Expand the “Assets” section in version 0.118 and download the arm APK file as shown in the image below

- After a successful download, install the application and you can get started with Termux on Android.
# Install Nethunter Kex App
- The Nethunter Kex application will enable you to access the Desktop Interface for Kali Linux on your Android. You can easily download and install the APK file from the Nethunter Store website
# Install Hacker's Keyboard
- install di play store
# Setup the Environment
- Launch Termux on your phone and update and upgrade the system using the command below.
- pkg update && pkg upgrade -y
- termux-setup-storage
- you will see a message like "Allow Termux access photos, media and files on your device." Click Allow. When done, execute the command below to install some packages needed to install Kali Linux on android
# Fetch and Run the Installer Script
- Up to this point, we have everything needed to install Kali on our Android device. First, we will need to download the installer script which we will use to download the Kali image file. Follow the steps below.

Launch Termux from the applications menu.

Execute the following apt command below to install the wget utility which we will use to fetch the installer script from GitHub.
- apt install wget
- Download the installer script from GitHub using the command below
- wget https://gitlab.com/kalilinux/nethunter/build-scripts/kali-nethunter-project/raw/master/nethunter-rootless/install-nethunter-termux
- When you run the ls command, you will see a file called 'install-nethunter-termux'. You need to make this script executable by running the command below.
- chmod +x install-nethunter-termux
- Now, run the installer script using the command below
- ./install-nethunter-termux
- Nethunter ARM64 (full): Comprehensive Kali image with a wide range of tools for an extensive experience.
- Nethunter ARM64 (minimal): Streamlined version with essential tools, suitable for limited storage or lighter installations.
- Nethunter ARM64 (nano): Compact Kali image with minimal tools for specific, lightweight use cases.
- In our case, we will install the Kali Nethunter (full) image. It is a large image and might take some time. However, it comes with all the tools you would expect to kickstart your penetration testing journey After successfully installing Kali Linux on your Android phone
# Launch Kali Linux on Android
- Up to this point, Kali Linux is downloaded and installed on your Android phone. However, you will notice that you are still not getting the Kali shell prompt. To launch Kali, type the command below and hit Enter
- nethunter
- cat /etc/os-release | grep "\bNAME="
# Enable Kali Linux Graphical User Interface on Android
- Up to this point, you can only use Kali Linux using the command-line prompt on the Termux. Luckily, there is a way you can easily access and use the default XFCE Desktop environment, which comes installed on Kali Linux. This procedure uses straightforward logic. We will use the Win-Kex utility. A tool that enables users running Kali Linux via WSL access the Kali Desktop Interface on their Windows PC. Kex works by creating a VNC session on Kali Linux, and you can access the running session graphically using a Kex-client utility like Nethunter-kex.
- Follow the steps below to get started.

Launch the Termux application and type nethunter to open the Kali Linux shell prompt.

On the Kali Linux console, type kex and hit Enter.

You will see a prompt to set up a VNC password. Enter your Password and confirm.

# NOTE:
- VNC passwords have a limit of up to 8 characters. If you set a password of more than eight characters, it is truncated to 8 (by default).
  
- Next, you will see a prompt to set a "view-only password." Type 'N' for no and hit Enter.

To start Kex on your Android phone, run the command below:
- kex start
# Connect to Kali Linux instance on Android
- Now, launch the Nethunter application and enter the settings shown in the image below. Luckily most of the fields are filled automatically. All you need to type is the Password. You don't need to type the VNC username.

- When done, click Connect. That will launch Kali Desktop on your Mobile Phone in landscape mode, as shown below.

- Congratulations! You are now running the full-featured Kali Linux operating system on your Android phone. Of course, navigating through the tiny menus can be a little difficult, but luckily you can use the cursor and using your phone touchscreen as the touchpad/mouse for control.
# stop the VNC server, switch to the Termux application and type the command below:
- kex stop
