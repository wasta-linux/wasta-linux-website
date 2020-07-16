---
title: GitHub Setup
type: docs
bookToc: true
---

![Wasta-Linux](/media/wasta-linux-round-128.png)

# Wasta-Linux: GitHub Setup

This page is part of the [Wasta-Linux customizing process](/home/customizing).

Follow the below steps in order establish your GitHub ID and register a
SSH key with GitHub in order to be ready to contribute to the
Wasta-Linux custom packages hosted on GitHub.

1. ## Sign up for a GitHub ID

    [*https://github.com/*](https://github.com/)

2. ## Create an Open SSH Key

    - **"Passwords and Keys" app:** Select ```File > New``` from the menu to create a Secure Shell Key (if you do not already have one: if you already have one you can skip ahead to step **3**)

        ![New Secure Shell Key](/media/home/customizing/github-setup/ssh1.png)

    - Give the key a descriptive name, ignore any Advance key options, and click "Just Create Key"

        ![Just Create Key](/media/home/customizing/github-setup/ssh2.png)

    - DO NOT set a passphrase when prompted, just leave it blank and click "OK" 2 times.

    - You should now see your SSH key in the "OpenSSH keys" section of the Passwords and Keys application:

        ![New Key Created](/media/home/customizing/github-setup/ssh3.png)

3. ## Add SSH Key to your GitHub account

    - *"Passwords and Keys" app:* Open the SSH key created in step 2 and go to the "Details" tab, noting the location of the folder.  Typically this would be the hidden ```.ssh``` folder in your user home.

        ![SSH Key Location](/media/home/customizing/github-setup/ssh4.png)

    - Open the ```id\_rsa.pub``` file (the "Public Key" for your SSH key) in the ssh folder and **copy the entire contents of the id\_rsa.pub file to your clipboard.**  The file should look something like this:

        ![Contents of id._rsa](/media/home/customizing/github-setup/ssh5.png)

    - Log into your GitHub account and click on your user name / icon in the top right of any GitHub page, and choose "Settings".  From the main "Settings" page you should see a "SSH keys" tab like this:

        ![Github Account](/media/home/customizing/github-setup/ssh6.png)

    - In the "SSH keys" tab, click "Add SSH key", entering a description in the "Title" field and pasting in the contents of  your id\_rsa.pub file from the clipboard in the "Key" field.  Click "Add key".

        ![GitHub Add Key](/media/home/customizing/github-setup/ssh7.png)

    - Your "SSH keys" tab should now list the key:

        ![GitHub List Key](/media/home/customizing/github-setup/ssh8.png)

4. ## Contact the Wasta-Linux team

    Please contact us through the [*Wasta-Linux Users
Forum*](https://groups.google.com/forum/#!forum/wasta-linux-users) after
you have created your GitHub account so we can add your GitHub ID as a
[*GitHub Wasta-Linux organization*](https://github.com/wasta-linux)
member.
