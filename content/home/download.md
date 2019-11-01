---
title: Downloads
type: docs
bookToc: false
---

<p align="center"> ![Wasta-Linux](../../img/wasta-linux-round-128.png)
# Wasta-Linux: Downloads

*If you are unsure of which download may be best for your hardware, please use the links at the bottom of this page to post to the Wasta-Linux Users list to ask for clarification.*

### {{< tabs "downloads" >}}

{{< tab "18.04" >}}

### [**Wasta-Linux-18.04.3-64Bit**](http://www.wastalinux.org/downloads/isos/wl-18-04-3/WL-18.04.3-64bit.iso)
* ***updated:*** 2019-08-30
* ***md5:*** f13a4cf5d18e8f40a5cfd0722dc1d814

***Notes:***

* **Based on Ubuntu 18.04 "Bionic"**
* **Interface:** *Cinnamon* is the default interface, with *Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by Ubuntu through **April 2023**
* **UEFI Compatible:** Fully Compatible with newer UEFI and Secure Boot features used by Windows 8+ computers
* **Linux Kernel:** 5.0 (due to Ubuntu's "Hardware Enablement Stack"... the original 18.04 release included Linux Kernel 4.15)
* **Paratext:** Paratext 8.0 / 9 Beta supported (Paratext 7.5 ***not*** available)
* **AMD Users:** *Use the below 18.04.1 ISO for Lenovo 14W and possibly other computers with a recent AMD Graphics processors*

{{< expand "Wasta-Linux 18.04.1 Hardware Compatibility Download" >}}
Wasta-Linux 18.04.1 may be needed if you experience any hardware compatibility issues with the 5.0 Linux Kernel included in Wasta-Linux 18.04.3.
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

* **Based on Ubuntu 16.04 "Xenial"**
* **Interface:** *Cinnamon* is the default interface, with *Ubuntu Unity* also installed
* **Long-Term Support:** Security updates provided by Ubuntu through **April 2021**
* **UEFI Compatible:** Fully Compatible with newer UEFI and Secure Boot features used by Windows 8+ computers
* **Linux Kernel:** 4.13
* **Paratext:** Paratext 7.5 **and** Paratext 8.0 supported
{{< /tab >}}
{{< /tabs >}}

## Wasta-Linux Installation Tips and Tricks:

* [**The above images can be put on a USB flash drive or DVD**]({{< relref "/tutorials/create-bootable-usb.md" >}}) just like a standard Ubuntu or Linux Mint ISO.

* [**Follow these instructions**]({{< relref "/home/ubuntu-migration.md" >}}) if you aren't starting with a Wasta-Linux ISO but rather want to upgrade your existing Ubuntu installation to Wasta-Linux.

* If you are wanting to do an "in-place upgrade" from a previous version of Wasta-Linux and don't have a separate home partition, you can [**follow this guide.**]({{< relref "/tutorials/inplace-upgrade.md" >}})

* If you are wanting to run Wasta-Linux in VirtualBox, [**first read these instructions.**]({{< relref "/tutorials/virtualbox-install.md" >}})

* To install Wasta-Linux to a portable, encrypted USB drive without touching the main OS on the computer, [**you can follow this guide.**]({{< relref "/tutorials/usb-install.md" >}})
