---
title: Downloads
type: docs
bookToc: false
---

![Wasta-Linux](/media/wasta-linux-round-128.png)

# Wasta-Linux: Downloads

*If you are unsure of which download may be best for your hardware, please use the links at the bottom of this page to post to one of the Wasta-Linux User Forums to ask for clarification.*

### {{< tabs "downloads" >}}

{{< tab "22.04" >}}

### [**Wasta-Linux-22.04.1-64Bit**](http://www.wastalinux.org/downloads/isos/wl-22-04-1/WL-22.04.1-64bit.iso)
* ***updated:*** 2023-01-25
* ***md5:*** ff08d80f79453dddbbb24493bd008bf7

***Notes:***

* **Based on _Ubuntu 22.04.1 "Jammy Jellyfish"_**
* **Interface:** *Cinnamon* is the default interface, with *Ubuntu Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2027**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 5.15
* **SIL Software:** Many SIL apps are available as traditional `.deb` packages for use in Wasta-Linux including the *App Builders*, *Adapt It*, and others. Due to a design decision beyond our control, you will need to use *Synaptic Package Manager* (pre-installed) to find these SIL software applications.

  However, traditional `.deb` versions of *.NET based SIL software* are not available for 22.04. Instead, `Flatpak` is used for distributing *Fieldworks* and *Bloom*, and `Snap` is used to distribute *Paratext (9.0)* and *Paratext Lite.* The *Software* application can be used to search for and install `flatpak` and `snap` applications.
{{< /tab >}}

{{< tab "20.04" >}}

### [**Wasta-Linux-20.04.5-64Bit**](http://www.wastalinux.org/downloads/isos/wl-20-04-5/WL-20.04.5-64bit.iso)
* ***updated:*** 2022-03-24
* ***md5:*** cab1cc4abd64cc872c8927ab166c17dd

***Notes:***

* **Based on _Ubuntu 20.04.5 "Focal Fossa"_**
* **Interface:** *Cinnamon* is the default interface, with *Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2025**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 5.13 (due to *Ubuntu's "Hardware Enablement Stack"* - the original 20.04 release included *Linux Kernel 5.4* Please contact us if your hardware requires this older kernel)
{{< /tab >}}

{{< tab "20.04 BT USB Image" >}}

## Coming Soon...
* ***updated:***
* ***md5:***
* ***download size:*** xxGB
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
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2025**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 5.8 (due to *Ubuntu's "Hardware Enablement Stack"* - the original 20.04 release included *Linux Kernel 5.4* Please contact us if your hardware requires the older *Linux Kernel 5.4*)
{{< /tab >}}

{{< tab "32-bit (18.04)" >}}

### [**Wasta-Linux-18.04.5-32Bit**](http://www.wastalinux.org/downloads/isos/wl-18-04-5-32bit/WL-18.04.5-32bit.iso)
*32-bit* is only needed for older computers (2010 and earlier) that do not support 64-bit. If you aren't certain you need *32-bit*, **please try Wasta-Linux 20.04 first!**

* ***updated:*** 2020-11-12
* ***md5:*** ccab8b18fec3b04d9b11bdfd0b5f5f02

***Notes:***

* **Based on _Ubuntu 18.04.4 "Bionic"_**
* **Interface:** *Cinnamon* is the default interface, with *Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2023**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 5.3 (due to *Ubuntu's "Hardware Enablement Stack"* - the original 18.04 release available below included *Linux Kernel 4.15* and may be needed for older hardware compatibility)
* **Paratext:** *Paratext 8 / 9* supported

***Notes:***

* **Interface:** *XFCE* is the default interface (more lightweight than *Cinnamon* for older, slower computers)
* **Last 32-bit Version:** *Ubuntu* no longer provides 32-bit packages. This means it will not be possible to make newer 32-bit versions of *Wasta-Linux*.
* **Installer Login:** Due to some minor bug, when starting the installer, it will prompt you for a login name and password. Please enter the following:
  * **Login:** live
  * **Password:** <blank> - just press *'Enter'*
{{< /tab >}}

{{< /tabs >}}

## *Wasta-Linux* Installation Tips and Tricks:

* [**The above images can be put on a USB flash drive or DVD**](/tutorials/create-bootable-usb) just like a standard *Ubuntu* or *Linux Mint* ISO.

* [**Follow these instructions**](/home/ubuntu-migration) if you aren't starting with a *Wasta-Linux* ISO but rather want to upgrade your existing *Ubuntu* installation to *Wasta-Linux*.

* If you are wanting to do an *"in-place upgrade"* from a previous version of Wasta-Linux and don't have a separate home partition, you can [**follow this guide.**](/tutorials/inplace-upgrade)

* If you are wanting to run *Wasta-Linux* in *VirtualBox*, [**first read these instructions.**](/tutorials/virtualbox-install)

* To perform a full installation of *Wasta-Linux* to a portable, encrypted USB drive without touching the main OS on the computer, [**you can follow this guide.**](/tutorials/usb-install)

* To use a pre-configured *Wasta-Linux* USB Image that can be run from a USB Drive without going through the full installation procedure, please click on the `USB Image` tab above for instructions.
