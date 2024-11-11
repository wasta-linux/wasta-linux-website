---
title: Downloads
type: docs
bookToc: false
---

![Wasta-Linux](/media/wasta-linux-round-128.png)

# Wasta-Linux: Downloads

*If you are unsure of which download may be best for your hardware, please use the link at the bottom of this page to post to the Wasta-Linux User Forum to ask for clarification.*

### {{< tabs "downloads" >}}

{{< tab "24.04" >}}

### [**Wasta-Linux-24.04.1**](https://www.wastalinux.org/downloads/isos/wl-24-04-1/WL-24.04.1.iso)
* ***updated:*** 2024-09-17
* ***md5:*** 5bf9ad7bbffb937eb288659536c44541

***Notes:***
* **Based on _Ubuntu 24.04.1 "Noble Numbat"_**
* **Interface:** *Cinnamon* is the default interface, with *Gnome (Ubuntu's default interface)* alternately available from the login screen
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2029**
* **Linux Kernel:** 6.8 - This kernel version will not change so you will have more stability to your system if all of your hardware works well with it. If you have hardware requiring a newer Linux Kernel, post to the Wasta-Linux User Forum (links below) to ask for assistance.
* **SIL Software Availability:** Many SIL apps are available as traditional `.deb` packages for use in Wasta-Linux including the *App Builders*, *Adapt It*, and others. Due to a security design decision beyond our control, you will need to use *Synaptic Package Manager* (pre-installed) to find these SIL software applications.
  * However, traditional `.deb` versions of *.NET based SIL software* are not available for 24.04. Instead, `Flatpak` is used for distributing *Fieldworks* and *Bloom*, and `Snap` is used to distribute *Paratext (9.0)* and *Paratext Lite.* The *Software* application can be used to search for and install these applications.
{{< /tab >}}

{{< tab "22.04" >}}

### [**Wasta-Linux-22.04.3-64Bit**](https://www.wastalinux.org/downloads/isos/wl-22-04-3/WL-22.04.3-64bit.iso)
* ***updated:*** 2023-08-17
* ***md5:*** dd5552d203db8512f448ceff1a556412

***Notes:***
* **Based on _Ubuntu 22.04.3 "Jammy Jellyfish"_**
* **Interface:** *Cinnamon* is the default interface, with *Ubuntu Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2027**
* **UEFI Compatible:** Fully compatible with newer *UEFI* firmware. *NOTE:* in early 2023 Ubuntu needed to update their *Secure Boot* keys, meaning you will need to disable *Secure Boot* in your machine's BIOS. Sorry for the inconvenience.
* **Linux Kernel:** 6.2 - Thanks to Ubuntu's *HWE (HardWare Enablement)* support. When Ubuntu releases newer Linux Kernels from their interim releases (23.10, etc.), you will automatically be upgraded to these newer kernels. For this reason, it is recommended to use the 24.04.1 ISO if your hardware runs well with it as this version will *NOT* have it's kernel version change.
* **SIL Software Availability:** Many SIL apps are available as traditional `.deb` packages for use in Wasta-Linux including the *App Builders*, *Adapt It*, and others. Due to a design decision beyond our control, you will need to use *Synaptic Package Manager* (pre-installed) to find these SIL software applications.
  * However, traditional `.deb` versions of *.NET based SIL software* are not available for 22.04. Instead, `Flatpak` is used for distributing *Fieldworks* and *Bloom*, and `Snap` is used to distribute *Paratext (9.0)* and *Paratext Lite.* The *Software Manager* application can be used to search for and install `flatpak` applications, and the *Snap Store* application can be used to search for and install `snap` applications.
{{< /tab >}}

{{< tab "20.04" >}}

### [**Wasta-Linux-20.04.5-64Bit**](https://www.wastalinux.org/downloads/isos/wl-20-04-5/WL-20.04.5-64bit.iso)
* ***updated:*** 2022-03-24
* ***md5:*** cab1cc4abd64cc872c8927ab166c17dd

***Notes:***

* **Based on _Ubuntu 20.04.5 "Focal Fossa"_**
* **Interface:** *Cinnamon* is the default interface, with *Gnome-Shell* also installed
* **Long-Term Support:** Security updates provided by *Ubuntu* through **April 2025**
* **UEFI Compatible:** Fully compatible with newer *UEFI* and *Secure Boot* features used by *Windows 8+* computers
* **Linux Kernel:** 5.13 (due to *Ubuntu's "Hardware Enablement Stack"* - the original 20.04 release included *Linux Kernel 5.4* Please contact us if your hardware requires this older kernel)
  * If your hardware is too new, then 20.04 may not boot correctly or have other hardware compatibility issues. In that case, you should use 24.04.
* **SIL Software Availability:** 20.04 is the last *Wasta-Linux* release that traditional `.deb` versions of *.NET based SIL software* are available for. This means that older versions of *Paratext 8*, *Paratext 9.0*, *Fieldworks*, and *Bloom* can be found and installed using the *Software Manager*.
  * *Snap* also available in 20.04, so *Paratext Lite* can be installed by running `sudo snap install paratextlite`. *Snap* packages unfortunately will not show in the *Software Manager* used in 20.04.
{{< /tab >}}

{{< /tabs >}}

## *Wasta-Linux* Installation Tips and Tricks:

* [**The above images can be put on a USB flash drive or DVD**](/tutorials/create-bootable-usb) just like a standard *Ubuntu* or *Linux Mint* ISO.

* [**Follow these instructions**](/home/ubuntu-migration) if you aren't starting with a *Wasta-Linux* ISO but rather want to upgrade your existing *Ubuntu* installation to *Wasta-Linux*.

* If you are wanting to do an *"in-place upgrade"* from a previous version of Wasta-Linux and don't have a separate home partition, you can [**follow this guide.**](/tutorials/inplace-upgrade)

* If you are wanting to run *Wasta-Linux* in *VirtualBox*, [**first read these instructions.**](/tutorials/virtualbox-install)

* To perform a full installation of *Wasta-Linux* to a portable, encrypted USB drive without touching the main OS on the computer, [**you can follow this guide.**](/tutorials/usb-install)
