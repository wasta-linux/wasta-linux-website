---
title: Downloads
type: docs
bookToc: false
---

![Wasta-Linux](/media/wasta-linux-round-128.png)

# Wasta-Linux: Downloads

*If you are unsure of which download may be best for your hardware, please use the links at the bottom of this page to post to one of the Wasta-Linux User Forums to ask for clarification.*

### {{< tabs "downloads" >}}

{{< tab "20.04" >}}

### [**Wasta-Linux-20.04.1-64Bit**](http://www.wastalinux.org/downloads/isos/wl-20-04-1/WL-20.04.1-64bit.iso)
* ***updated:*** 2020-09-20
* ***md5:*** 0d58bc159522fba7a76f0c561989050a

***Notes:***

* **Based on _Ubuntu 20.04.1 "Focal Fossa"_**
* **Interface:** *Cinnamon* is the default interface, with *Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2025**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 5.4
{{< /tab >}}

{{< tab "18.04" >}}

### [**Wasta-Linux-18.04.4-64Bit**](http://www.wastalinux.org/downloads/isos/wl-18-04-4/WL-18.04.4-64bit.iso)
* ***updated:*** 2020-04-14
* ***md5:*** 1f3913eead2cb36cad777fe41657cd04

***Notes:***

* **Based on _Ubuntu 18.04.4 "Bionic"_**
* **Interface:** *Cinnamon* is the default interface, with *Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2023**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 5.3 (due to *Ubuntu's "Hardware Enablement Stack"* - the original 18.04 release available below included *Linux Kernel 4.15* and may be needed for older hardware compatibility)
* **Paratext:** *Paratext 8 / 9* supported (*Paratext 7.5* ***not*** available)

---

### [**Wasta-Linux-18.04.1-64Bit**](http://www.wastalinux.org/downloads/isos/wl-18-04-1/WL-18.04.1.2-64bit.iso)
*Wasta-Linux 18.04.1* may be needed if you experience any hardware compatibility issues with the *5.3 Linux Kernel* included in *Wasta-Linux 18.04.4*. **Please Try Wasta-Linux 18.04.4 First!**

* ***updated:*** 2018-09-27
* ***md5:*** ce7f69957d92f11130732f37771dbac8

---

### [**Wasta-Linux-18.04.5-32Bit**](http://www.wastalinux.org/downloads/isos/wl-18-04-5-32bit/WL-18.04.5-32bit.iso)
*32-bit* is only needed for older computers (2010 and earlier) that do not support 64-bit. If you aren't certain you need *32-bit*, **please try Wasta-Linux 18.04.4 first!**

* ***updated:*** 2020-11-12
* ***md5:*** ccab8b18fec3b04d9b11bdfd0b5f5f02

***Notes:***

* **Interface:** *XFCE* is the default interface (more lightweight than *Cinnamon* for older, slower computers)
* **Last 32-bit Version:** *Ubuntu* no longer provides 32-bit packages. This means it will not be possible to make newer 32-bit versions of *Wasta-Linux*.
* **Installer Login:** Due to some minor bug, when starting the installer, it will prompt you for a login name and password. Please enter the following:
  * **Login:** live
  * **Password:** <blank> - just press *'Enter'*
{{< /tab >}}

{{< tab "18.04 BT USB Image" >}}

### [**Wasta-Linux-18.04.3-BT-USB**](http://www.wastalinux.org/downloads/other/usb-image/wasta-bt-2019-11-22.img.bz2)
* ***updated:*** 2019-11-22
* ***md5:*** 611439bc8d4cb489461d47de51eb7684
* ***download size:*** 42GB
* ***default encryption passphrase:*** wastabt.123
* ***default login password:*** user.123
* [**USB Setup Instructions**](/tutorials/expand-usb-image)

***Notes:***

* **Bootable USB Image:** Expand the file to a 64GB USB stick and boot directly from any host machine.
* **Encrypted:** The image is encrypted so that any data from the USB system will not be readable if the USB is attempted to be used by others.
* **BT Software Pre-Installed:** The following software for BT use is pre-installed:
    * Adaptit, Audacity, Bloom, Fieldworks, Logos, Paratext 8, Paratext 9, Script___ App Builder, Pathway, Xiphos (Sword)
    * ***Note:*** You will need your own registration keys to activate *Paratext* or *Logos*.
* **Based on _Ubuntu 18.04 "Bionic"_**
* **Interface:** *Cinnamon* is the default interface, with *Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2023**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 5.0 (due to *Ubuntu's "Hardware Enablement Stack"* - the original 18.04 release included *Linux Kernel 4.15*)
{{< /tab >}}

{{< /tabs >}}

## *Wasta-Linux* Installation Tips and Tricks:

* [**The above images can be put on a USB flash drive or DVD**](/tutorials/create-bootable-usb) just like a standard *Ubuntu* or *Linux Mint* ISO.

* [**Follow these instructions**](/home/ubuntu-migration) if you aren't starting with a *Wasta-Linux* ISO but rather want to upgrade your existing *Ubuntu* installation to *Wasta-Linux*.

* If you are wanting to do an *"in-place upgrade"* from a previous version of Wasta-Linux and don't have a separate home partition, you can [**follow this guide.**](/tutorials/inplace-upgrade)

* If you are wanting to run *Wasta-Linux* in *VirtualBox*, [**first read these instructions.**](/tutorials/virtualbox-install)

* To perform a full installation of *Wasta-Linux* to a portable, encrypted USB drive without touching the main OS on the computer, [**you can follow this guide.**](/tutorials/usb-install)

* To use a pre-configured *Wasta-Linux* USB Image that can be run from a USB Drive without going through the full installation procedure, please click on the `USB Image` tab above for instructions.
