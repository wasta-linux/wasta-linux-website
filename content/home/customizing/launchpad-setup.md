---
title: Maintain a Custom Package
type: docs
bookToc: false
---

<p align="center"> ![Wasta-Linux](../../../img/wasta-linux-round-128.png)

# Wasta-Linux: Maintain a Custom Package

This page is part of the [Wasta-Linux customizing process]({{< relref "/home/customizing.md" >}}).

Git is used for version control of all the Wasta-Linux custom packages. There is a [Wasta-Linux organization](https://github.com/wasta-linux) on GitHub that contains separate GitHub repositories for each Wasta-Linux custom package. Any changes that are pushed up to these repositories are automatically copied every 6 hours to Launchpad, which is Ubuntu's site for managing software. Once the code is in Launchpad, there is another automatic process that builds the actual software packages and places them in the [Wasta-Linux Testing Launchpad PPA](https://launchpad.net/%7Ewasta-linux/+archive/wasta-testing). Once the 'Regional Customizer' (you!) confirms that the package from the Wasta-Linux Testing PPA is good, any Wasta-Linux Launchpad member can copy it to the [main Wasta-Linux Launchpad PPA](https://launchpad.net/~wasta-linux/+archive/ubuntu/wasta). This main PPA is already included in every Wasta-Linux system, so once the packages exist in the PPA, all Wasta-Linux users will be able to install them when they update their system.

So, as a maintainer of a Wasta-Linux custom package, all you will need to do is get your changes to GitHub, and after that you should find your updated package available for install in the next day when you update your system.

Here then are the steps for maintaining a Wasta-Linux custom package. I will use the ```wasta-custom-eth``` package as an example.

1. ### Setup (only needs to be done the first time)

    1. Create a GitHub account and register a SSH key with GitHub

        - Follow the steps in this [GitHub setup guide]{{< relref "/home/customizing/github-setup.md" >}})

0.2: Install needed dependencies on your machine

- *Terminal command:* ***sudo apt-get install build-essential devscripts dh-make dpkg-dev git***

0.3: Configure git on your computer

- *Terminal command:* ***git config --global user.email "you@example.com"***
- *Terminal command:* ***git config --global user.name "Your Name"***

0.4: Adjust your profile so it will automatically enter your name and email when building the Wasta-Linux custom packages for local testing

- *Terminal command:* ***echo 'export DEBFULLNAME=Your\\ Name' &gt;&gt; \~/.profile***

- **NOTE the "\\" delimiter to account for the space in the name (between "Your" and "Name" in this example)**

- *Terminal command:* ***echo 'export DEBEMAIL=you@example.com' &gt;&gt; \~/.profile***
- The user name and email address should match those used in step 0.3 above.
- You will have to logout / login for these settings to take effect

0.5: Create a PGP key

- A PGP key is required to create a "local test package" of your Wasta-Linux custom package (see section 3 below)

<!-- -->

- *"Passwords and Keys" app:* "File | New" and then choose "PGP Key"

<!-- -->

- - IMPORTANT: do NOT enter a "key comment", only enter "name" and "email", or else there will be problems with using it later.
- The user name and email address should match those used in step 0.3 above.
- Setting the key to never expire should be OK.
- After entering a password, the key will be generated.

- Please wait, eventually the new key will show up under the "GnuPG Keys" tab, but unfortunately the application does not give much feedback during this key generation process

0.6: Create a "wasta-packages" folder on your machine to use for the source code of the Wasta-Linux custom packages

0.7: Clone desired Wasta-Linux custom package to your wasta-packages folder

- Using the Wasta-Linux GitHub organization page, go to the wasta-custom-eth GitHub repository and click the "copy to clipboard" icon in the "SSH clone url:" section on the right bottom of the page.

- Right click on the "wasta-packages" folder created in 0.5 above and choose "Open in Terminal"
- *Terminal command:* ***git clone &lt;pasted contents from your clipboard&gt;***

- *Example:* ***git clone git@github.com:wasta-linux/wasta-custom-eth.git***

- The "wasta-custom-eth" folder containing the current source code will now exist in your "wasta-packages" folder.

1\. Get Current Source

- - Right click on the "wasta-packages/wasta-custom-eth" folder and choose "Open in Terminal"
- *Terminal command:* ***git pull***

2\. Make changes to code

***2.1: Make any needed changes to the code***

- - Here is a basic reference to the files in the "debian" folder, which is necessary to build the package after it finally arrives at Launchpad:

- **debian/control: Most important debian file.** Defines dependencies and other package details.
- **debian/install:** Defines files installed on the system when the package is installed.

- Typically Wasta-Linux custom packages have an "install-files" folder where all the files installed by a package reside. Confirm in this "debian/install" file.
- Sometimes there is also a package name folder such as "wasta-custom-eth" in this example, that is installed to "/usr/share/wasta-custom-eth". Again, this "debian/install" file will define these things.

- **debian/changelog:** Do NOT manually update this file, but instead use "dch" (see below).
- **debian/postinst:** Script executed after install of package. This should just call /usr/share/wasta-custom-eth/wasta-custom-eth-postinst.sh (I want this script easily accessible to others for reference: talk to me more if you want more gory details).

2.2: Use "dch" to create the new version and enter comments regarding what changes you will make

- - Terminal command: ***dch --newversion 0.1.5*** (replace 0.1.5 with your new version)

- if prompted, choose "/bin/nano" as the editor, as it is the easiest to use.

- When using nano, the "\^" character is entered using the "Control" key on your keyboard.

- Replace "UNRELEASED" with your series name

- 12.04: **precise**
- 14.04: **trusty**

- Enter some reasonable comments to document your changes. Reference older changelog entries for examples.
- Enter "\^O" (again, Control + o) to save your changes.
- Enter "\^X" (again, Control + X) to exit nano.

3\. Build new local test version

- *Terminal command:* ***debuild -b***

- Builds a ".deb" package file for local testing
- You must have a PGP key set up that will sign the packages. Creating the PGP key is above in step 0.5
- The resulting .deb will be created "up" one directory (in the wasta-packages folder created in step 0.6)
- "Lintian" checks are done looking for any standards violations. Clean up any errors found and re-run until it is clean.

- You can Google the full lintian phrase to see the warning description.

- The following "warnings" can be ignored:

- *Terminal output:* ***dpkg-gencontrol: warning: Depends field of package wasta-custom-eth: unknown substitution variable \${shlibs:Depends}***

- Use the created .deb to install manually on another local machine for testing to ensure all changes are applied correctly.

- The testing machine must have the same "architecture" (32 bit or 64 bit) as the machine you created the .deb on.

4\. Use git to commit changes and push to GitHub repository

- **IMPORTANT: clean up from debuild -b process!**

- the "debuild -b" process from step 3 above creates some temporary build files that we don't want to keep. Clean them up! **This is important or else the next step to add files to git will add these temporary files, which we don't want.**

- *Terminal command:* ***debclean***

- If you have added any new files to the folder, you will need to 'add' them to git so they are part of the version control

- This is why it is important to run "***debuild clean***" first so that the temporary debian files won't be added to version control!
- *Terminal command:* ***git add -A***

- All files in the wasta-custom-eth folder not already part of git version control will be added

- Confirm git status (can be done at any time)

- *Terminal command:* ***git status***

- Commit changes to git

- *Terminal command:* ***git commit -am "&lt;short commit message&gt;"***

- *Example:* ***git commit -am "Adding LibreOffice Extension"***

<!-- -->

- Push changes to GitHub

- *Terminal command:* ***git push***

5\. Use Launchpad to test the automatically built package in the Wasta-Linux Testing PPA and then manually copy to the main Wasta-Linux PPA

5.1: Monitor Package build in Launchpad

- - Wasta-Linux Team Launchpad site: [**https://launchpad.net/\~wasta-linux**](https://launchpad.net/%7Ewasta-linux)

- Under "Related Projects" in the bottom right there should be a link to each Wasta-Linux custom package project

- The Launchpad Wasta-Linux custom package project should automatically pull in any changes from the GitHub repository every 6 hours.
- The Launchpad Wasta-Linux custom package project should automatically build packages from the updated source code every 24 hours.

- If you need to speed up either of these 2 processes, you can trigger them manually from the [**Launchpad Wasta-Linux**](https://launchpad.net/~wasta-linux) custom package project's code and recipes. Please contact the Wasta-Linux team if you need assistance with this process.
- By default, the packages are built in the [**Wasta-Linux Testing PPA**](https://launchpad.net/~wasta-linux/+archive/ubuntu/wasta-testing).

5.2: Test package created in Wasta-Linux Testing PPA

- - Ensure you have the Wasta-Linux Testing PPA added to your system

- *Terminal command:* ***sudo add-apt-repository ppa:wasta-linux/wasta-testing***

- Update your package lists

- *Terminal command:* ***sudo apt-get update***

- Install package

- *Terminal command:* ***sudo apt-get install wasta-custom-xyz***

5.3: Copy package from Wasta-Linux Testing PPA to main Wasta-Linux PPA

- - Any Wasta-Linux Launchpad member can copy packages between PPAs.

- [**Follow this guide**](https://sites.google.com/site/wastalinux/home/customizing/launchpad-setup) to become a Wasta-Linux Launchpad member.

- Package is now available to all Wasta-Linux users.

[]{#anchor}


