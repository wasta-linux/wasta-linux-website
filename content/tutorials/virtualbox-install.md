---
title: Virtualbox Installation
type: docs
bookToc: false
---

![Wasta-Linux](/media/wasta-linux-round-128.png)
# Wasta-Linux VirutalBox Installation

In general, [Wasta-Linux] ({{< relref "/" >}}) runs fine in VirtualBox *after the VirtualBox Guest Additions have been installed on the Wasta-Linux guest virtual machine and settings are made correctly.* Before the VirtualBox Guest Additions are installed, it will not be possible to enable "3D Graphics", which Cinnamon requires, and you will get a warning message when logging in that you are in "Software Rendering Mode". There are a few quirks to getting these "Guest Additions" installed that are documented here.

VirtualBox setup notes:

- Choose "Ubuntu" as the Linux version when installing Wasta-Linux in VirtualBox.

- Ensure that 3D Graphics are enabled in the VirtualBox settings (see screenshot below):

![VirtualBox 3D Settings](/media/tutorials/virtualbox-install/vb-3d-settings.png)

After ensuring that 3D Graphics are being used (see above) in the settings, start Wasta-Linux in VirtualBox and then after logging in, from the menu choose `Devices > Insert Guest Additions CD image...` and follow the prompts to complete the Guest Additions installation.

You will be asked for an administrative password *(the password you created for the user at install time has administrative permissions, so use this password).* A terminal window will launch, and may ask if you want to replace the older version of Guest Additions, what do you want to do?

Type `yes` at this prompt and then click `Enter` to continue and the Virtualbox Guest Additions should install successfully. You will need to shutdown and restart for 3D graphics to be enabled. Then when logging into Cinnamon, you should NOT get the "Software Rendering" message.
