![](Pictures/100002010000019400000094814C377F678DB1A2.png){width="10.689cm" height="3.916cm"}
=============================================================================================

[]{#anchor}How to turn Ubuntu 18.04 into Wasta-Linux 18.04
==========================================================

-   ***NOTE:*** Wasta-Linux only targets Ubuntu LTS releases, such as
    18.04, 16.04, etc.  Interim short-term Ubuntu releases such as
    17.10, 18.10, etc. are not supported.

To take an existing Ubuntu 18.04 system and change it into Wasta-Linux
18.04, perform the following steps from a terminal:

### []{#anchor-1}1. Get the Wasta-Linux core package installed:

The following terminal commands *(perform them one at a time)* are
needed to install the all-essential wasta-core-bionic package, which is
the foundation for Wasta-Linux:

***sudo add-apt-repository ppa:wasta-linux/wasta\
sudo apt-get update*****\
*****sudo apt-get install wasta-core-bionic*****\
*****sudo apt-get update***

-   -   ***NOTE:*** the second "apt-get update" is needed since
        wasta-core-bionic adds additional repositories to your computer,
        such as packages.sil.org and the wasta-apps ppa.  You then need
        this second apt-get update to make the packages from those
        repositories available for installation.
    -   ***NOTE:*** you may want to restart your system at this point

### []{#anchor-2}2. Install Cinnamon *(recommended but optional)*:

You do not have to install the Cinnamon desktop interface and can
continue using Ubuntu's Unity desktop instead, but most Wasta-Linux
tutorials and development focus revolve around the Cinnamon interface. 
Also note that even if you do install Cinnamon, the Ubuntu Unity desktop
interface will not be removed, so you can continue using it or Cinnamon,
whichever you prefer.\
\
The following terminal command will install Cinnamon and set it as the
default desktop interface:

*\
**sudo add-apt-repository ppa:wasta-linux/cinnamon-3-8\
****sudo apt-get update\
sudo apt-get install wasta-cinnamon-bionic***

-   -   ***NOTE:*** You will be prompted to choose a 'login manager'. 
        Please select lightdm for the best experience.
    -   ***NOTE:*** If your system still logs into Ubuntu's default
        Gnome-Shell you can click the icon in the upper right of the
        user login box from the login screen and choose "Cinnamon".

### []{#anchor-3}**3. Run the Wasta-Linux setup script** *(recommended but optional)*:

The following terminal command will perform these steps to give you the
full Wasta-Linux experience:

-   Remove unwanted apps (you will be prompted so you can answer "N" to
    the question if you don't want to remove anything)
-   Install all software updates
-   Install all default Wasta-Linux apps

***sudo wasta-initial-setup***

-   -   ***NOTE:*** If you want to run this full process
        "non-interactively", so that the app removals and other bits are
        done without prompting you, please append the "auto" parameter
        like this:

***sudo wasta-initial-setup auto***

-   -   ***NOTE:*** You will definitely want to restart your system
        after this process has finished.

### []{#anchor-4}Congratulations, you are now running Wasta-Linux!

[]{#anchor-5}


