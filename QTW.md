# 📂 Project WTQ: Windows 10 (32-bit) Experimental Build

**Date:** February 17, 2026  
**Operator:** Matthew Noel Coto ("NostalgicUniSec")  
**Status:** In Progress  

---

## 🎯 Objective
To deploy a **32-bit Windows 10** environment inside a Qubes OS Standalone VM to test architectural limitations, memory constraints, and driver compatibility (Qubes Windows Tools) in a hardened, air-gapped scenario.

---

## 🛠 Hardware Context ("The Bunker")
* **Host:** Qubes OS 4.2 (Laptop)
* **Input:** 8BitDo Retro Mechanical Keyboard (Famicom Edition)
* **Security:** Privacy Hood deployed for visual hardening (Anti-Shoulder Surfing)
* **Vibe:** "NostalgicUniSec" / Cyberdeck Art Installation

---

## ⚙️ VM Configuration
* **Name:** `win10-32bit-test`
* **Class:** StandaloneVM (HVM)
* **Kernel:** None (Direct boot)
* **Architecture:** x86 (32-bit)
* **Memory (RAM):** Locked at **3500 MB** (3.5 GB) to match 32-bit addressable limits.
* **Storage:** Private Volume resized to **32+ GB** to accommodate ISO extraction.

---

## 📝 Execution Log

### Phase 1: Preparation & ISO Acquisition
* **Action:** Downloaded Windows 10 (32-bit) ISO via `work` qube.
* **Hurdle:** Encountered `Disk Space Full` error during download. Default AppVM private storage (2GB) was insufficient.
* **Fix:** Resized `work` qube private storage to **20GB+** via Qubes Manager.
    * *Command Verification:* `df -h /home` (Confirmed >20GB available).
    * *Result:* Download successful.

### Phase 2: VM Construction (Terminal Method)
Constructed the VM using `dom0` terminal for precision control over HVM parameters.


#### 1. Create the Standalone VM (Label red for "Danger/Windows")
```bash
qvm-create --class StandaloneVM --label red win10-32bit-test
```

#### 2. Set Virtualization Mode to HVM (Hardware Virtual Machine)
```bash
qvm-prefs win10-32bit-test virt_mode hvm
```

#### 3. Detach Linux Kernel (Crucial for Windows boot)
```bash
qvm-prefs win10-32bit-test kernel ''
```

#### 4. Hard-lock Memory to 32-bit Limit (Prevent installer crashes)
```bash
qvm-prefs win10-32bit-test memory 3500
```

```bash
qvm-prefs win10-32bit-test maxmem 3500
```
