---
title: Wasta-Layout
type: docs
bookToc: false
---

<p align="center"> ![Wasta-Linux](../../img/wasta-linux-round-128.png)

# Wasta-Layout: Cinnamon Desktop Layout Settings Utility

## What is it?

Wasta-Layout is a simple utility for changing the layout of the panel (taskbar) and other items of the desktop interface in Cinnamon (the default desktop interface of Wasta-Linux).  Different preset layout configurations have been added to Wasta-Layout to provide different user experiences for Cinnamon.

## How do I use it?

Here is a screenshot of the Wasta-Layout dialog:

![Wasta-Layout dialog](../../img/wasta-apps/wasta-layout/wasta-layout-dialog.png)

Simply select the desired layout and click OK. A prompt will then ask if the selected layout should be set as the "System Default" which means any newly created users will be created using this layout. To not annoy other existing users on the system, Wasta-Layout will not change their existing desktop layouts.

Below are descriptions and screenshots of the various Wasta-Layout desktop layouts:

## Default

The **'default'** layout option of Wasta-Layout largely matches the defaults directly from the Cinnamon development team.

*Notable items include:*
- The bottom panel and Main Menu are similar to Windows XP
- Application windows are ***not*** grouped

<p align="center"> ![Wasta-Layout 'default' layout](../../img/wasta-apps/wasta-layout/wasta-layout-default.png)
<p align="center"> ![Wasta-Layout 'default' hover](../../img/wasta-apps/wasta-layout/wasta-layout-default-hover.png)

## Redmond7

The **'redmond7'** layout is meant to match Windows 7's interface more closely than the Cinnamon default layout.

*Notable differences compared to the 'default' layout include:*
- Application windows are grouped together, with a number in the top left of showing the number of running windows for each application.
- The bottom panel is slightly taller in order to give larger panel icons

<p align="center"> ![Wasta-Layout 'redmond7' layout](../../img/wasta-apps/wasta-layout/wasta-layout-redmond7.png)
<p align="center"> ![Wasta-Layout 'redmond7' hover](../../img/wasta-apps/wasta-layout/wasta-layout-redmond7-hover.png)

## Cupertino

The **'cupertino'** layout is meant to loosely match Apple's macOS / OSX interface.

*Notable differences compared to the 'default' layout include:*
- The panel is placed at the top
- A 'dock' is placed at the bottom: it will hide automatically when windows are placed over it. Dock items can 'zoom' when hovering over them
- The panel is semi-transparent (but becomes non-transparent when a window is placed next to it)

*Notable shortcomings compared to Apple's macOS / OSX interface:*
- There is no 'Global AppMenu' (application menus will show in the application's own window rather than in the main system panel)

<p align="center"> ![Wasta-Layout 'cupertino' layout](../../img/wasta-apps/wasta-layout/wasta-layout-cupertino.png)

## Unity

The **'unity'** layout is inspired by Ubuntu's Unity interface, which was Ubuntu's default from 2011 through 2017.

*Notable differences compared to the 'default' layout include:*
- The panel is placed at the top
- A non-hiding 'dock' is placed on the left side.
- The Main Menu is the top item in the dock, and has the shutdown menu and favorites removed.
- The shutdown menu is in the top right.
- The panel and dock are semi-transparent (but become non-transparent when a window is placed next to them)

*Notable shortcomings compared to Ubuntu Unity's interface:*
- There is no 'Global AppMenu' (application menus will show in the application window rather than in the main system panel)
- There is no 'HUD' ("heads up display"): this is the ability in Unity to quickly find application menu items by pressing ALT then typing to search for the desired setting.  The global menu is required for this functionality, and at this time there is no easy way to add a global menu to Cinnamon.
- The end result is that the panel in the Wasta-Layout Unity interface is largely unused (except for the right side).  So unfortunately this means that vertical space is not as efficiently used as under Unity.

<p align="center"> ![Wasta-Layout 'unity' layout](../../img/wasta-apps/wasta-layout/wasta-layout-unity.png)

## Widescreen

The **'widescreen'** layout seeks to maximize vertical space for today's widescreen displays.

*Notable differences compared to the 'default' layout include:*
- The panel is placed on the left side, with no bottom panel
- Application windows are grouped together, with a number in the top left of showing the number of running windows for each application
- Some of the 'system tray icons' in the bottom left of the panel can be be collapsed to reduce the space they take up in the panel
- The panel is semi-transparent (but becomes non-transparent when a window is placed next to it)

<p align="center"> ![Wasta-Layout 'widescreen' layout](../../img/wasta-apps/wasta-layout/wasta-layout-widescreen.png)

{{< columns >}}

<p align="center">Widescreen layout with the system tray collapsed:

<p align="center"> ![Wasta-Layout 'widescreen' collapsed](../../img/wasta-apps/wasta-layout/wasta-layout-widescreen-collapsed.png)

<--->

<p align="center">Widescreen layout with the system tray expanded:

<p align="center"> ![Wasta-Layout 'widescreen' expanded](../../img/wasta-apps/wasta-layout/wasta-layout-widescreen-expanded.png)

{{< /columns >}}

