# Adding TempleOS to a Standalone Qube

* **Name:** TempleQube
* **Color:** Yellow
* **Note:** You don't have to use the same name or color; you can pick your own.

## Step 1: Download the ISO
Download the ISO file through the TempleOS website: [https://templeos.org/Downloads/](https://templeos.org/Downloads/)
> **CRITICAL NOTE:** Do NOT forget which qube you downloaded the file to, since we need to get the `.iso` from that qube. I will use the qube named **"work"** for this guide.

## Step 2: Building the TempleQube
We will build the qube through the **Dom0 terminal** (Xfce Terminal).

1.  **Create the Qube:** This will create a standalone qube with a yellow icon named "TempleQube". We use HVM mode since TempleOS is its own operating system.
    ```bash
    qvm-create --class StandaloneVM --label yellow --property virt_mode=hvm TempleQube
    ```

2.  **The "No Kernel" Step:** Even though we set `virt_mode=hvm`, we need to tell Qubes that TempleOS is on its own kernel and not on a Linux kernel.
    ```bash
    qvm-prefs TempleQube kernel ''
    ```

3.  **Memory & Network:** We will set memory to a static 512MB and disable networking since we don't need it.
    ```bash
    qvm-prefs TempleQube memory 512
    qvm-prefs TempleQube maxmem 512
    qvm-prefs TempleQube netvm ''
    ```

## Step 3: Fix Settings in Qubes Manager
1.  Go to the **"Q" menu** (top left) > **Qubes Tools** > **Qubes Manager**.
2.  Right-click **TempleQube** and select **Settings**.
3.  Go to the **Advanced** tab.
4.  Look for "Boot qube from CDROM/DVD" (or "Boot from device").
5.  Select **"From file in qube"**.
6.  Choose the qube where you downloaded the file (e.g., **"work"**).
7.  Select the ISO file path (e.g., `/home/user/Downloads/TempleOS.ISO`) and click **OK**.

## Step 4: Booting and Installation
Go back to the **Dom0 terminal** and type the following command to start the VM with the CDROM attached:

```bash
qvm-start TempleQube --cdrom work:/home/user/Downloads/TempleOS.ISO

Enjoy TempleOS, your frist non-Linux operating system.
You can learn HolyC, a C-like language only for this OS
  If you already know C/C++ you'll understand how HolyC works.
