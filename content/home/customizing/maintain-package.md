---
title: Maintain a Custom Package
type: docs
bookToc: false
---

![Wasta-Linux](/media/wasta-linux-round-128.png)

# Wasta-Linux: Maintain a Custom Package

This page is part of the [Wasta-Linux customizing process]({{< relref "/home/customizing.md" >}}).

Git is used for version control of all the Wasta-Linux custom packages. There is a [Wasta-Linux organization](https://github.com/wasta-linux) on GitHub that contains separate GitHub repositories for each Wasta-Linux custom package. Any changes that are pushed up to these repositories are automatically copied every 6 hours to Launchpad, which is Ubuntu's site for managing software. Once the code is in Launchpad, there is another automatic process that builds the actual software packages and places them in the [Wasta-Linux Testing Launchpad PPA](https://launchpad.net/~wasta-linux/+archive/wasta-testing). Once the 'Regional Customizer' (you!) confirms that the package from the Wasta-Linux Testing PPA is good, any Wasta-Linux Launchpad member can copy it to the [main Wasta-Linux Launchpad PPA](https://launchpad.net/~wasta-linux/+archive/ubuntu/wasta). This main PPA is already included in every Wasta-Linux system, so once the packages exist in the PPA, all Wasta-Linux users will be able to install them when they update their system.

So, as a maintainer of a Wasta-Linux custom package, all you will need to do is get your changes to GitHub, and after that you should find your updated package available for install in the next day when you update your system.

Here then are the steps for maintaining a Wasta-Linux custom package. I will use the ```wasta-custom-eth``` package as an example.

1. ## Setup

    (only needs to be done the first time)

    1. ### GitHub setup

        You will need to create a GitHub account and register your SSH key with GitHub. Follow the steps in this [GitHub setup guide]({{< relref "/home/customizing/github-setup.md" >}}).

    2. ### Install dependencies

        You will need to install some dependencies on your machine in order to have the necessary tools for building packages.

        - ***Terminal \* command:***

          ```
          sudo apt-get install build-essential devscripts dh-make dpkg-dev git
          ```

    3. ### Configure git

        Git is used for version control so will need to be configured so that any changes you make will correctly be linked to your id.

        - ***Terminal \* commands:*** _(execute commands 1 at a time)_
          ```
          git config --global user.email "you@example.com"
          git config --global user.name "Your Name"
          ```

    4. ### Adjust your profile

        You need to adjust your profile settings so that your name and email will automatically be inserted when building the Wasta-Linux custom packages for local testing

        - ***Terminal \* command:***
          ```
          echo 'export DEBFULLNAME=Your\ Name' >> ~/.profile
          ```
          - ***NOTE:*** the ```\``` delimiter is needed to account for the space in the name (between ```Your``` and ```Name``` in this example)

        - ***Terminal \* command:***
            ```
            echo 'export DEBEMAIL=you@example.com' >> ~/.profile
            ```

            - ***NOTE:*** the user name and email address should match those used in step **"1.c"** above.

        You will have to logout / login for these settings to take effect.

    5. ### Create a PGP key

        A PGP key is required to create a "local test package" of your Wasta-Linux custom package (see section 3 below)

        - Open the ```Menu > Accessories > Passwords and Keys``` application

        - Choose ```File > New``` and then choose "PGP Key"

            - ***Important:*** do ***NOT*** enter a "key comment", only enter "name" and "email", or else there will be problems with using it later.
            - The user name and email address should match those used in step **"1.c"** above.
            - Setting the key to never expire should be OK.
            - After entering a password, the key will be generated.

                - Please wait, eventually the new key will show up under the "GnuPG Keys" tab, but unfortunately the application does not give much feedback during this key generation process

    6. ### Create working folder

        You need a folder on your machine to use for the source code of the Wasta-Linux custom packages. You may create it in the location of your choice, such as your ```Documents``` folder. A suggestion is to name the folder ```wasta-packages```, so it would look like this: ```/home/<username>/Documents/wasta-packages/```.

    7. ### Clone package

        * Using the [Wasta-Linux GitHub organization page](https://github.com/wasta-linux), search for the ```wasta-custom-xyz``` GitHub repository that you would like to modify and click the ```copy to clipboard``` icon in the ```SSH clone url:``` section on the righthand side of the bottom of the page.

        - Right click on the ```wasta-packages``` folder created in step **"1.f"** above and choose "Open in Terminal"
        - ***Terminal \* command:***
          ```
          git clone <pasted contents from your clipboard>
          ```
        - ***Example:***
          ```
          git clone git@github.com:wasta-linux/wasta-custom-eth.git
          ```

        The "wasta-custom-eth" folder containing the current source code will now exist in your "wasta-packages" folder.

2. ## Get current source

    Right click on the "wasta-packages/wasta-custom-eth" folder and choose "Open in Terminal"

    * ***Terminal \* command:***
      ```
      git pull
      ```

3. ## Make changes to code

    Make any changes to the code, then we are ready to update the debian packaging files that are used to build the new version of the package.

    1. ### Debian folder references

        Here is a basic reference to the files in the "debian" folder, which is necessary to build the package after it finally arrives at Launchpad:

        - **debian/control: Most important debian file.** Defines dependencies and other package details.
        - **debian/install:** Defines files installed on the system when the package is installed.

            Typically Wasta-Linux custom packages have an "install-files" folder where all the files installed by a package reside. Confirm in this "debian/install" file.

            Sometimes there is also a package name folder such as "wasta-custom-eth" in this example, that is installed to "/usr/share/wasta-custom-eth". Again, this "debian/install" file will define these things.

        - **debian/changelog:** Do NOT manually update this file, but instead use ```dch``` (see below).
        - **debian/postinst:** Script executed after install of package. This should just call ```/usr/share/wasta-custom-eth/wasta-custom-eth-postinst.sh``` (I want this script easily accessible to others for reference: talk to me more if you want more gory details).

    2. ### Update changelog

        Use ```dch``` to create the new version and enter comments regarding what changes you will make

        - ***Terminal \* command:***
          ```
          dch --newversion 0.1.5
          ```
            - Replace ```0.1.5``` with your new version

            - if prompted, choose ```/bin/nano``` as the editor, as it is the easiest to use.

                - When using nano, the "^" character is entered using the ```Ctrl``` key on your keyboard.

            - Replace ```UNRELEASED``` with your series name

                - 16.04: **xenial**
                - 18.04: **bionic**

            - Enter some reasonable comments to document your changes. Reference older changelog entries for examples.
            - Enter ```^O``` (again, ```Ctrl + O```) to save your changes.
            - Enter ```^X``` (again, ```Ctrl + X```) to exit nano.

4. ## Build local test version

    - ***Terminal \* command:***
      ```
      debuild -b
      ```
      - Builds a ".deb" package file for local testing
      - You must have a PGP key set up that will sign the packages. Creating the PGP key is above in step **"1.e"**
      - The resulting .deb will be created "up" one directory in the ```wasta-packages``` folder created in step **"1.f"**
      - "Lintian" checks are done looking for any standards violations. Clean up any errors found and re-run until it is clean.

        - You can "Google" the full lintian phrase to see the warning description.
        - The following "warnings" can be ignored:

            - ***Terminal output:***
              ```
              dpkg-gencontrol: warning: Depends field of package wasta-custom-eth: unknown substitution variable ${shlibs:Depends}
              ```

        - Use the created .deb to install manually on another local machine for testing to ensure all changes are applied correctly.

            - The testing machine must have the same "architecture" (32 bit or 64 bit) as the machine you created the .deb on.

5. ## Commit changes and push

    Git will now be used to commit the changes and then push them to GitHub.

    1. ### Clean up

        _Important:_ first clean up from the ```debuild -b``` process!

        The ```debuild -b``` process from step 4 above creates some temporary build files that we don't want to keep. Clean them up! ***This is important or else the next step to add files to git will add these temporary files, which we don't want.***

        - ***Terminal \* command:***
          ```
          debclean
          ```

    2. ### Add new files

        If you have added any new files to the folder, you will need to 'add' them to git so they are under version control.

        - This is why it is important to run ```debclean``` first so that the temporary debian files won't be added to version control!
        - ***Terminal \* command:***
          ```
          git add --all
          ```

        - All files in the ```wasta-custom-xyz``` folder not already part of git version control will be added to it

    3. ### Confirm git status

        (can be done at any time)

        - ***Terminal \* command:***
          ```
          git status
          ```

    4. ### Commit changes

        Until your changes are "committed" they are not updated in git.

        - ***Terminal \* command:***
          ```
          git commit -am "<short commit message>"
          ```

            - ***Example:***
            ```
            git commit -am "Adding LibreOffice Extension"
            ```

    5. ### Push changes

        Pushing changes will transfer the git commits / updates to GitHub.

        - ***Terminal \* command:***
          ```
          git push
          ```

6. ## Launchpad package creation

    Launchpad will auto-build the package from GitHub as described below.

    1. ### Monitor Launchpad test build

        - [Wasta-Linux Team Launchpad site](https://launchpad.net/~wasta-linux)

            - Under "Related Projects" in the bottom right there should be a link to each Wasta-Linux custom package project

        - _Launchpad_ will automatically import source code from Github every 6 hours.

        - _Launchpad_ will automatically build new packages every 24 hours in the [Wasta-Linux Testing PPA](https://launchpad.net/~wasta-linux/+archive/wasta-testing).

            - Please contact the Wasta-Linux team if you need either of these processes expedited

    2. ### Test package

        Before distributing the new package to all Wasta-Linux users, it is advisable to test install the package first, only submitting to other users after it is confirmed to be error free.

        1. #### Add Wasta Testing PPA

            Ensure you have the Wasta-Linux Testing PPA added to your system

            - ***Terminal \* command:***
              ```
              sudo add-apt-repository ppa:wasta-linux/wasta-testing
              ```

        2. #### Update your package lists

            - ***Terminal \* command:***
              ```
              sudo apt-get update
              ```

        3. #### Install test package

            - ***Terminal \* command:***
              ```
              sudo apt-get install wasta-custom-xyz
              ```

    3. ### Copy package to main PPA

        After confirming the package in the Wasta-Testing PPA is ready to be distributed to other users, it must be copied to the main Wasta-Linux PPA. Any Wasta-Linux Launchpad member can copy packages between PPAs.

        - [Follow this guide]({{< relref "/home/customizing/launchpad-setup.md" >}}) to become a Wasta-Linux Launchpad member.

        The package is now available to all Wasta-Linux users.

---
**\*** _To open the Terminal, in Wasta-Linux go to ```Menu > Administration > Terminal```, or press the following keys at the same time: ```Ctrl + Alt + T```_
