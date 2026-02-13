We are adding the Temple Operating System into a standalone qube
Name   -   TempleQube
Color  -   Yellow
  -  Note you don't have to use the same name or color, you can pick your own.
Step one, download the iso file thorught the TempleOS website: https://templeos.org/Downloads/ > Click TempleOS.ISO
  CRITICAL NOTE!: Do NOT forget the qubes you download sence we need to get the .iso from that qubes file. I will use work for now-on.
Step two, building the TempleQube through the Dom0 terminal: it will be name Xfce Terminal.
  @dom0:~$ [qvm-create --class StandaloneVM --label yellow --property virt_mode=hvm TempleQube]
This will 'create' the 'standalone' qube in a 'yellow' qube icon w/ the name TempleQube in the Qubes Manger.
We will use HVM since TempleOS is it's own operating system.
    The "No Kernel" Step
Eventhough you set it in the virt_mode=hvm, we need to tell qubes that TempleOS is on its own kernel and not on a Linux Kernal.
    @dom0:~$ [qvm-prefs TempleQube kernel]
    -  This will force to boot itself and not on linux.
Memory & Network, we will set it to a static 512, and disable network since we don't need it to function.
  @dom0:~$ [qvm-prefs TempleQube memory 512] NOTE: there will not prompt you a messiage, it will just bring back to command.
  @dom0:~$ [qvm-prefs TempleQube maxmem 512]
  @dom0:~$ [qvm-prefs TempleQube netvm'']
  one done we will go to the Qubes Manger to clear up some setting.
Step 3, Fix thing in settings
  Let's go to:
  Qubes Manager on the "Q" menu tab to the top left side where the couge wheel is > Qubes Tools > Qubes Manager.
Click on TempleQube > Setting > Advanced Advanced > Boot qube from DISC or block device > click, from file in qube, choose "work" > and add the /home/user/Documents/TempleOS.ISO > OK
  Once click on OK from Setting let's go to terning it on and installation
Step 4 Booting and Installation.
Now let's go back to Dom0 terminal on the Xfce Terminal and type (or copy and past) this
  @dom0:~$ [qvm-start TempleQube --cdrom work:/home/user/Downloads/TempleOS.ISO] and press enter.
