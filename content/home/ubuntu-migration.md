---
title: Ubuntu Migration
type: docs
bookToc: false
---

![Ubuntu to Wasta-Linux](/media/home/ubuntu-migration/ubu-2-wasta.png)

# How to turn Ubuntu into Wasta-Linux

To take an existing Ubuntu 22.04 system and change it into Wasta-Linux 22.04, from a Terminal **\*** perform the following steps:

- ***NOTE:*** Wasta-Linux only targets Ubuntu LTS _(**L**ong **T**erm **S**upport)_ releases, such as **22.04**, **20.04**, etc. Interim short-term Ubuntu releases such as **23.04**, **22.10**, etc. are _**not**_ supported.

1. ## Get the Wasta-Linux core package installed:

    The following Terminal **\*** commands *(perform them one at a time)* are needed to install the all-essential `wasta-core-focal` package, which is the foundation for Wasta-Linux:

    ```
    sudo add-apt-repository ppa:wasta-linux/wasta
    sudo apt-get update
    sudo apt-get install wasta-core
    sudo apt-get update
    ```
    - ***NOTE:*** the second `apt-get update` is needed since `wasta-core` adds additional repositories to your computer, such as `packages.sil.org` and the `wasta-apps` ppa. You then need this second `apt-get update` to make the packages from those repositories available for installation.

    - ***NOTE:*** you may want to restart your system at this point

2. ## Install Cinnamon:

    _(recommended but optional)_

    - You do not have to install the Cinnamon desktop interface and can continue using Ubuntu's Unity desktop instead, but most Wasta-Linux tutorials and development focus revolve around the Cinnamon interface.Also note that even if you do install Cinnamon, the Ubuntu Unity desktop interface will not be removed, so you can continue using it or Cinnamon, whichever you prefer.

    - The following Terminal **\*** commands *(perform them one at a time)* will install Cinnamon and set it as the default desktop interface:

      ```
      sudo add-apt-repository ppa:wasta-linux/cinnamon-5-4
      sudo apt-get update
      sudo apt-get install wasta-cinnamon
      sudo wasta-cinnamon-upgrade
      ```

    - ***NOTE:*** If you are prompted to choose a _'login manager'_, please select `lightdm`.

    - ***NOTE:*** If your system still logs into Ubuntu's default Gnome-Shell you can click the icon in the upper right of the user login box from the login screen and choose "Cinnamon".

3. ## Run the relevant Wasta-Linux upgrade / setup script:

    _(recommended but optional)_

    - ### Option 1:

      - Run the `wasta-system-upgrade` Terminal **\*** command:

        ```
        sudo wasta-system-upgrade
        ```

      - This will perform the following steps:
        - #### Install all software updates

        - #### Install all default Wasta-Linux apps

        - #### Enable `zswap` for better virtual RAM performance

    - ### Option 2:

      - Run the `wasta-initial-setup` Terminal **\*** command:

        ```
        sudo wasta-initial-setup
        ```

      - In addition to the steps executed by the `wasta-system-upgrade` script, this script will perform these additional steps:
        - #### Remove unwanted apps
          - You will be prompted so you can answer `No` to the question if you don't want to remove the unwanted apps

        - #### Install the Ubuntu "Hardware Enablement" stack
          - This will upgrade the _Linux Kernel_ and the _x-server display server_ to the _"Hardware Enablement"_ verisons distributed by Ubuntu, which is recommended for newer hardware.

        - #### Set `redmond7` as the default [**Cinnamon-Layout**](/wasta-apps/cinnamon-layout)
          - Of course this is only performed if Cinnamon is installed _(see above)_

        - #### Remove installed snap packages to save space on future ISOs

    - ***NOTE:*** For either of the above 2 options if you want to run the full process _"non-interactively"_, so that the app removals and other bits are done without prompting you, please append the `auto` parameter like this: `sudo wasta-system-upgrade auto`

    - ***NOTE:*** You will definitely want to restart your system after this process has finished.

4. ## Congratulations, you are now running Wasta-Linux!

---
**\*** _To open the Terminal, in Wasta-Linux go to `Menu > Administration > Terminal`, or press the following keysat the same time: `Ctrl + Alt + T`_
