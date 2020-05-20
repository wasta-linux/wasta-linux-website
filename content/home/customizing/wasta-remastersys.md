---
title: Wasta-Remastersys
type: docs
bookToc: true
---

![Wasta-Linux](/media/wasta-linux-round-128.png)

# Wasta-Remastersys

This page is part of the [Wasta-Linux customizing process]({{< relref "/home/customizing.md" >}}).

The Wasta-Linux ISOs are created using Wasta-Remastersys. Wasta-Remastersys is also pre-installed in Wasta-Linux so that anyone can use it to create their own customized Wasta-Linux ISO.

In order to create your own custom ISO, you can follow these steps:

1. ## Install Wasta-Linux

    It is preferable to do this on a "clean test machine" designated for this process.

2. ## Customize Wasta-Linux

    Follow either method listed on the [Wasta-Linux customizing page]({{< relref "/home/customizing.md" >}}).

    - ***NOTE:*** Due to limitations of the ISO specification, there is a 4GB max size limitation on ISOs created with Wasta-Remastersys.

3. ## Copy all of your customizations to the "default user profile"

    In order to have the customizations you have made for the current user act as the defaults for new users, you need to copy the current user's files to the "new user profile template folder" located at /etc/skel.

    To copy all the configuration and settings you can use the `wasta-remastersys-skelcopy` Terminal **\*** command.  You need to provide the username that you want to serve as the basis for the "default user profile":

    - ***Terminal \* command:***

    ```
    sudo wasta-remastersys-skelcopy <username>
    ```

    If you need additional items from a user's home directory (such as training materials or other resources) copied to the default user profile folder, you will need to copy them manually.

    You can confirm the default profile is set correctly by creating a new user onyour computer and then logging in as that new user.  Everything should be correct (including all settings such as default user background, etc.).  If not, you need to adjust the default user profile more and try again.

4. ## Configure Wasta-Remastersys

    The Remastersys configuration settings are stored in the following file:

    ```
    /etc/wasta-remastersys/wasta-remastersys.conf
    ```

    Notable things you may want to edit in this file include:

    - **LIVECDLABEL=** Here you list the CD Label Name for the ISO.
    - **CUSTOMISO=** This is the created ISO filename.
    - **INCLUDES=** Here you can specify any additional folder you want to include in the remastered ISO.  An example would be /home/data.  If you included any files you want to distribute to all users in a 'wasta-custom-xyz package', this won't be necessary.

5. ## Run Wasta-Remastersys

    Once you are ready, run this command from the Terminal **\*** to start Wasta-Remastersys:

    - ***Terminal command:***

    ```
    sudo wasta-remastersys dist
    ```

6. ## Finished

    After the above command completes, your ISO (and a md5 checksum for it) will be ready in the
`/home/wasta-remastersys/wasta-remastersys` folder.  Install it on a USB drive and give it a test!

---
**\*** _To open the Terminal, in Wasta-Linux go to `Menu > Administration > Terminal`, or press the following keys at the same time: `Ctrl + Alt + T`_
