---
title: Expand Image to USB Drive
type: docs
bookToc: true
---

<p align="center"> ![Wasta-Linux](../../img/wasta-linux-round-128.png)

# Wasta-Linux: Expand USB Image to a USB Drive

A Wasta-Linux USB image is pre-installed and pre-configured system ready to be put on a USB drive that can be shared with others without each user needing to follow the full ['Bootable USB' installation process]({{< relref "/tutorials/create-bootable-usb.md" >}}). You will need a 64GB (or larger) high quality USB3 drive to use for your encrypted USB Wasta-Linux system.

1. ## Download Wasta-Linux Bootable USB Image

    Find the Bootable USB image from the [download page]({{< relref "/home/download.md" >}}). ***Note the large size of image files*** due to them being a fully pre-installed and pre-configured system!

2. ## Decompress Image file

    The image file is compressed in .bz2 format to reduce the size of the download. To decompress, in a standard Wasta-Linux system, right-click and choose "Extract Here":

    <p align="center"> ![Extract Here](../../img/tutorials/expand-usb-image/extract-here.png)

    The result should be a .img file which is now ready to be expanded to a USB drive.

3. ## Insert and Identify USB Drive Root

    Insert your USB drive and use "Disks" from the Main Menu to identify which device it is:

    <p align="center"> ![Identify Drive](../../img/tutorials/expand-usb-image/identify-drive.png)

    In this example, the USB drive is listed as `/dev/sdd1`. **The root of this USB drive is then `/dev/sdd`.**

    **Important:** Make sure you correctly identify your device! Choosing a wrong device will wipe out your data!

4. ## Expand Image to USB Drive

    The most simple and least error-prone way to expand the image file to the USB drive is to use `ddrescue` in the terminal. In an empty space of your folder with the `.img` file in it, right-click and choose `Open in Terminal` and proceed with the below command:

    ````
    sudo ddrescue --force ./wasta-bt-2019-11-22.img /dev/sde
    ````

    Note that `--force` is needed since it will overwrite the existing data on the USB drive. Again make sure from `Step 3` that you have identified your USB drive correctly!

    `ddrescue` does a nice job of giving feedback on how much time is remaining. Since the `.img` file is 60+ GB in size, it will take some time!

    ````
    $ sudo ddrescue --force ./wasta-bt-2019-11-22.img /dev/sdd
    [sudo] password for rik:
    GNU ddrescue 1.22
         ipos:    2310 MB, non-trimmed:     0 B,  current rate:  23789 kB/s
         opos:    2310 MB, non-scraped:     0 B,  average rate:  38512 kB/s
    non-tried:   59194 MB,  bad-sector:     0 B,    error rate:       0 B/s
      rescued:    2310 MB,   bad areas:     0,        run time:          1m
    pct rescued:    3.75%, read errors:     0,  remaining time:         45m
                               time since last successful read:          0s
    Copying non-tried blocks... Pass 1 (forwards)
    ````

    In the above example, my USB drive will take up to 45 minutes for the `.img` file to be expanded to it. Not all USB3 drives are created equal!

4. ## Boot USB Device

    After `ddrescue` finishes, your USB drive should be ready to boot from another machine. Use the shortcut required on your machine to select the USB drive as the boot selection.

    You can find the default disk encryption password and user login password from the Download page notes.

5. ## Change Default Passwords

    To change the disk encryption password, use `Disks` from the `Main Menu` and select the USB device (ignore the 'Block Device' entries). Then select the `LUKS` partition, and click the `gear` and `Change Passphrase...` as in this screenshot:

    <p align="center"> ![Disks](../../img/tutorials/expand-usb-image/disks.png)

    To change the user login password, use `Account Details` from the `Main Menu` and click on the current `Password` *(it will be masked by dots):*

    <p align="center"> ![Account Details](../../img/tutorials/expand-usb-image/account-details.png)




