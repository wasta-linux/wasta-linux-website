---
title: Wasta-Resources
type: docs
bookToc: false
---

<p align="center"> ![Wasta-Resources](../../img/wasta-apps/wasta-resources/wasta-resources-128.png)

# Wasta-Resources: Centralized Documentation Distribution

## What is it?

Basically Wasta-Resources is just a standard place in Wasta-Linux to put any read-only reference materials you want, and it also adds a launcher to open to the location in a file browser, so that this location is easy findable by users from the Main Menu.

The location is `/usr/share/wasta-resources`.  Any package can place items here (We would recommend a sub-folder for your region).

For example, the SSG (Sudan group) Wasta-Resources package is called `wasta-ssg-resources`. It puts a folder called `SSG Resources` in `/usr/share/wasta-resources`. Inside this folder are keylists for the various SSG keyman keyboards.

Another example is the `wasta-custom-eth` package, which creates a symlink in the `/usr/share/wasta-resources` folder to `/usr/share/doc/kmfl-keyboard-sil-ethiopic/readme.htm`, so that again users can easily find the keyboard reference for this Keyman keyboard.

In both cases, Wasta-Resources simply provides a central location to place reference files for users.  It is unlikely that normal users are going to find the `/usr/share/doc/kmfl-keyboard-sil-ethiopic/readme.htm` file otherwise!

## How do I add materials to Wasta-Resources?

For people wanting to distribute materials this way, it would require you to maintain packages in the Wasta-Linux software repository, which is documented as part of the [Wasta-Linux customizing process]({{< relref "/home/customizing.md" >}}).

It is really easy for us to initially set up the Wasta-Resources packages, so if you want to work with us offline to give us whatever materials you want to distribute to your users, we can create the first`wasta-xyz-resources` package, after which any future modifications to this package will be made directly by you, the regional customizer. [Follow this guide to maintain 'wasta-custom-xyz' custom packages]({{< relref "/home/customizing/maintain-package.md" >}}).
