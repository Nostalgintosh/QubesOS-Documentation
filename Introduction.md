# QubesOS Introducation
Q/ Why should I use QubesOS and what make is different from other operating systems in both Linux and non-Linux operating system?
A/ Unlike Windows, MacOS, OS/2, and Linux Distrobutions QubesOS core philosophy is security by compartmentalization makes it one of the most secure operating systems

  by isolating through compartmentalizing each qube/a you can sperate your work life, your personal life, and other lives trough qubes/a.
  -   /a qubes are VM boxes that sperate work, life, &c., compartments so non can be corrupted through internal and external means.
Before installing QubesOS you need the right hardware that is combatible for the operating system, unlike others QubesOS need some types of hardware needed to run.

  -  NOTE: you can find it in the Qubes Hardware Compatibility list > https://www.qubes-os.org/hcl/
  -  or buy Qubes Certified hardware > https://doc.qubes-os.org/en/latest/user/hardware/certified-hardware/certified-hardware.html
  
  If you are not sure what are the system requirments you can find them here
    https://doc.qubes-os.org/en/latest/user/hardware/system-requirements.html

For the Minimum
-  It will need a 64-bit Intel or AMD processor also known as x86_64, x64, and AMD64, 6 GB RAM memory, and 32 GB free space storage
For the Remcommended
- https://doc.qubes-os.org/en/latest/user/hardware/system-requirements.html

Note: If you know the *Fedora's installation prosses,* Qubes installation will be familiar to you since it is the simular to installing a Fedora Distro.

However in short you first add your language and keyboard layout then you'll and the necessary drivers to intall and store the OS.
This is where you will add your user name and password. You can also a Graphic User Interface or *GUI* or choose the commandline for adding or removing your qubes. How you want, one selected you'll start the prosses of installation. Note this will take awhile so propare youself some coffee and wait...

Ones done and rebooted you go to the next setup, if you will like add pre-made template and what Xfce distro to pick Fedora or Debian and other things you may or may not want on you Qubes Operating System. inshort you'll done with the installation and setting up your OS, and now it time to configrate you OS for what you will need.

You'll have the opitions to have pre-made templete one done with the installation and greated with the setup amoung other things. The pre-made include premade template like Fedora Xfce with pre-made qubes name, personal, work, untrusted and vault.

  Note if you what to maxamize as much a possible either on a desktop or a laptop you'll need to know how manage your pass and know when it's too much.
  The Ram is esstinal to know you limiations of the hardware and the software, and by using **Qubes Dynamic Memory** you will understand

Once all finished you'll be greated with the univeral interface of the operating system and the "Q" button on the top-left. This is were your qubes, templates and other settings live.
next to "Q" is where the windows live browser, terminal, system settings &c. are in.
On the top-right, biginning on the left to right you will see the virtual desktops, the time, voluime and others that you see in others OSes. There is a Qubes button that you will see which qubes is taking what hardware like RAM & CPU.


## Understanding basic commandline
To understand the Qubes Operating System you'll need to understand the Xfce Terminal in both Dom0 and the qubes terminal itself, there both the same terminal so you don't need to know different commands in the terminal just which one is approitate to use. We are frist start by the basic command from Linux follow by Qubes what should be use and not be use from both Dom0 terminal and the qube terminal.
  ##### Note! Dom0 is only for the creation of *qubes* and nothing else. Do Not use it for anything else other than the bar minimun.

### Understnad Linuxs commands
To understand QubesOS you'll need to know linux itself, so knowing some Linux commandline is essintal in both Linux and Qubes Operating System. Here are the common (but not all) commands that you will need to know.

#### Meaning *Print Working Directory* that tells you were you are in the terminal or koncle.
```bash
pwd
```
#### This means *Change Directory* to change were you are.
```bash
cd
```
#### To lest folders on what cd you are in.
```bash
ls
```
#### To create folders.
```bash
mkdir
```
#### To remove folders
```bash
rmdir
```
### Understanding Qubes commands
