---
title: Customizing
type: docs
bookToc: false
---

![Wasta-Linux](/media/wasta-linux-round-128.png)

# Wasta-Linux: Customizing for your Needs

[Wasta-Linux] (/" >}}) is intended to be used as a base for regionally-localized Linux "customized" distributions specific to locations' needs (fonts, keyboards, applications, settings, included reference documents, etc.). 

Should you be interested in being a "regional customizer" of Wasta-Linux, please use the forums linked at the bottom of this page and someone will contact you.

There are 2 primary Wasta-Linux customizing methods, both of which can be used to [create custom Wasta-Linux ISOs](/home/customizing/wasta-remastersys) to re-distribute to users:

1. ## Manual customization

    Basically, install Wasta-Linux on a clean test system, and make the adjustments you want manually.  Then follow the [process to create a custom Wasta-Linux ISO](/home/customizing/wasta-remastersys).  If you make future modifications, you can re-create the ISO.  But, any customizations you make in the future that you want to distribute to *existing* users that installed your previous ISO will need to be individually made on each machine.  Due to this limitation, see method 2 below.

2. ## Create a ```wasta-custom-xyz``` package

    The main advantage of creating a ```wasta-custom-xyz``` package is that any future adjustments you make to your customizations will be automatically re-distributed to anyone with the wasta-custom-xyz package installed when they update their system.  Here is an overview of the process to create and maintain a ```wasta-custom-xyz``` package:

    1. ### Create a ```wasta-custom-xyz``` Package:

        Work with the Wasta-Linux team to create a new "package" called ```wasta-custom-xyz``` with all your desired customizations included.  The Wasta-Linux team will create the first version of this package for you.  Once this package is created, installing ```wasta-custom-xyz``` on any Wasta-Linux computer will include all of your customizations.

        Examples of customizations that can be included in a ```wasta-custom-xyz``` package include:

        - ***LibreOffice Default Settings:*** Use .doc, .xls extensions, enable complex text layout, set default language settings, etc.

        - ***Additional Keyboards:*** Install additional language keyboards.

        - ***Additional Fonts:*** Install additional fonts

        - ***Additional Applications:*** Install applications on ALL computers with wasta-custom-xyz such as Paratext, AdaptIt, FieldWorks, etc.

        - ***System Default Settings:*** Customize settings such as the default background image, touchpad behavior, default "application favorites", etc.

        - ***Wasta-Menus Default List:*** Customize the default Applications that are included in Wasta-Menus.

        - ***Reference Documents:*** Include a folder of reference documents that can optionally be linked to each users Home Directory.

    2. ### Maintain the ```wasta-custom-xyz``` Package:

        Ideally any future modifications to this 'wasta-custom-xyz' package will be made directly by you, the regional customizer. [Follow this guide to maintain 'wasta-custom-xyz' custom packages](/home/customizing/maintain-package).

    3. ### (Optional) Create a Custom Wasta-Linux ISO:

        As with method 1 above, you can install Wasta-Linux on a clean test system, then install your ```wasta-custom-xyz``` package, and then follow the [process to create a custom Wasta-Linux ISO](/home/customizing/wasta-remastersys).
