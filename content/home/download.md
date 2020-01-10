---
title: Downloads
type: docs
bookToc: false
---

<p align="center"> ![Wasta-Linux](../../img/wasta-linux-round-128.png)
# Wasta-Linux: Downloads

*If you are unsure of which download may be best for your hardware, please use the links at the bottom of this page to post to one of the Wasta-Linux User Forums to ask for clarification.*

### {{< tabs "downloads" >}}

{{< tab "18.04" >}}

### [**Wasta-Linux-18.04.3-64Bit**](http://www.wastalinux.org/downloads/isos/wl-18-04-3/WL-18.04.3-64bit.iso)
* ***updated:*** 2019-08-30
* ***md5:*** f13a4cf5d18e8f40a5cfd0722dc1d814

***Notes:***

* **Based on _Ubuntu 18.04 "Bionic"_**
* **Interface:** *Cinnamon* is the default interface, with *Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2023**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 5.0 (due to *Ubuntu's "Hardware Enablement Stack"* - the original 18.04 release included *Linux Kernel 4.15*)
* **Paratext:** *Paratext 8/9* supported (*Paratext 7.5* ***not*** available)
* **AMD Users:** *Use the below 18.04.1 ISO for Lenovo 14W and possibly other computers with a recent AMD Graphics processors*

{{< expand "Wasta-Linux 18.04.1 Hardware Compatibility Download" >}}
*Wasta-Linux 18.04.1* may be needed if you experience any hardware compatibility issues with the *5.0 Linux Kernel* included in *Wasta-Linux 18.04.3*
### [**Wasta-Linux-18.04.1-64Bit**](http://www.wastalinux.org/downloads/isos/wl-18-04-1/WL-18.04.1.2-64bit.iso)
* ***updated:*** 2018-09-27
* ***md5:*** ce7f69957d92f11130732f37771dbac8
{{< /expand >}}
{{< /tab >}}

{{< tab "16.04" >}}
### [**Wasta-Linux-16.04.4-64Bit**](http://www.wastalinux.org/downloads/isos/wl-16-04-4/WL-16.04.4.2-64bit.iso)
* ***updated:*** 2018-04-04
* ***md5:*** 5de5238868ceab725e2bbc914b1d471e

### [**Wasta-Linux-16.04.4-32Bit**](http://wastalinux.org/downloads/isos/wl-16-04-4/WL-16.04.4-32bit.iso)
* ***updated:*** 2018-04-04
* ***md5:*** 378bab914f86f208af021146a68c38ea

***Notes:***

* **Based on _Ubuntu 16.04 "Xenial"_**
* **Interface:** *Cinnamon* is the default interface, with *Ubuntu Unity* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2021**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 4.13
* **Paratext:** *Paratext 7.5* **and** *Paratext 8/9* supported
{{< /tab >}}

{{< tab "18.04 BT USB Image" >}}

### [**Wasta-Linux-18.04.3-BT-USB**](http://www.wastalinux.org/downloads/other/usb-image/wasta-bt-2019-11-22.img.bz2)
* ***updated:*** 2019-11-22
* ***md5:*** 611439bc8d4cb489461d47de51eb7684
* ***download size:*** 42GB
* ***default encryption passphrase:*** wastabt.123
* ***default login password:*** user.123
* [**USB Setup Instructions**]({{< relref "/tutorials/expand-usb-image.md" >}})

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

* [**The above images can be put on a USB flash drive or DVD**]({{< relref "/tutorials/create-bootable-usb.md" >}}) just like a standard *Ubuntu* or *Linux Mint* ISO.

* [**Follow these instructions**]({{< relref "/home/ubuntu-migration.md" >}}) if you aren't starting with a *Wasta-Linux* ISO but rather want to upgrade your existing *Ubuntu* installation to *Wasta-Linux*.

* If you are wanting to do an *"in-place upgrade"* from a previous version of Wasta-Linux and don't have a separate home partition, you can [**follow this guide.**]({{< relref "/tutorials/inplace-upgrade.md" >}})

* If you are wanting to run *Wasta-Linux* in *VirtualBox*, [**first read these instructions.**]({{< relref "/tutorials/virtualbox-install.md" >}})

* To perform a full installation of *Wasta-Linux* to a portable, encrypted USB drive without touching the main OS on the computer, [**you can follow this guide.**]({{< relref "/tutorials/usb-install.md" >}})

* To use a pre-configured *Wasta-Linux* USB Image that can be run from a USB Drive without going through the full installation procedure, please click on the `USB Image` tab above for instructions.
