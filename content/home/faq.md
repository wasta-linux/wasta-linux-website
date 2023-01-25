---
title: FAQ
type: docs
bookToc: false
---

![Wasta-Linux](/media/wasta-linux-round-128.png)

# Wasta-Linux: Frequently Asked Questions

Below are answers to some of the more common questions you may have about Wasta-Linux. First, a question and response that lays the foundation for Wasta-Linux:

## Why Linux?
One colleague answered the question "Why Linux" concisely using 3 main points. In brief, Linux is:

* **Partner friendly:** share with everyone, not only privledged organizations that have corporate license keys
* **Budget friendly:** not only does it not have a cost, it will also save support time
* **Customizing friendly:** adapt Linux to your use case, rather than having to adapt your usage to the limitations of a locked-down operating system that may not have you in mind as their target user base

Basically it is about freedom (not just "free as in no cost"), which means freedom to customize for our situation and for our specific users (see more below on this topic), freedom for _all_ to use it, and "free from viruses." **\*** For more on these freedoms, please read the ["case study" on our organization's move from Windows to Linux in NE Africa](/home/why-linux).

##### **\*** _Yes, eventually there may be Linux viruses, but its design is inherently more secure than Windows which was originally designed for single-user "non-networked" computers. Over the years Windows has applied security fixes in an "ad-hoc fashion" to try to account for today's always online environment, but many inherent vulnerabilities remain._

---

Click on a question below to see the response:

{{< expand "Which Linux desktop and distribution is Wasta-Linux based on?" >}}
With Ubuntu being recognized as the market leader in the Linux ecosystem, it was determined that using Ubuntu as a base for Wasta-Linux is the best choice. Using Ubuntu as a base ensures the broadest compatibility with Linux applications for Wasta-Linux.

However, the default interface, called a *'desktop environment'* in Linux, used by Ubuntu proved challenging to use as it was not familiar enough for users coming from a Windows environment. After a lot of testing with several different Linux desktops, Cinnamon, created by the Linux Mint team, was chosen as the default interface for Wasta-Linux. For those that aren't interested in adhering to a Windows-style interface, Cinnamon is flexible enough to be able to be reconfigured to match layouts inspired by macOS or Ubuntu's Unity.
{{< /expand >}}

{{< expand "What customizations are included in Wasta-Linux?" >}}
For the curious, here is a summary of some of the most significant modifications made to Wasta-Linux when compared to stock Ubuntu plus the Cinnamon desktop interface:

* ***"SIL ready":*** The SIL Linux repository is included and standard SIL fonts have been added, so that applications such as Paratext, Bloom, Fieldworks, Adapt It, WeSay and kmfl (Keyman) are ready for installation from the Software Center.

* ***Several applications added, several others removed.*** Notable additions include:
  * [**Wasta-Backup:**](/wasta-apps/wasta-backup) simple "version backup" utility
  * [**Wasta-Offline:**](/wasta-apps/wasta-offline) offline software updates and installs
  * [**Cinnamon-Layout:**](/wasta-apps/cinnamon-layout) desktop layout settings utility
  * [**Wasta-Menus:**](/wasta-apps/wasta-menus) limits the visible applications in the Main Menu
  * [**Wasta-Resources:**](/wasta-apps/wasta-resources) centralized distribution of reference and documentation materials
  * **Shotcut:** Non-linear video editing software
  * **GoldenDict:** Offline (and online using Wikipedia or other sources) Dictionary / Thesaurus
  * **Modem Manager GUI:** USB 3G modem tool for balance check and top-up commands
  * **Pinta:** simple to use "MS Paint" alternative
  * [**Kiwix:**](/tutorials/kiwix) offline simple English version of Wikipedia *(due to it's size - 1.6 GB - it is not installed by default in Wasta-Linux)*
  * **Klavaro:** typing tutor
  * *some useful command-line utilities such as:*
      * **wavemon:** a wifi network diagnostic tool
      * **traceroute**
      * **iperf:** a network throughput test tool

* ***Centralized update and distribution of "future Wasta customizations":*** No more being "stranded" as seems to happen with Ubuntu LTS releases.
{{< /expand >}}

{{< expand "What is the Wasta-Linux background story?" >}}
Wasta-Linux development began in 2011-2012 in NE Africa (أهلا وسهلا) where it became apparent that the efforts of a couple IT workers would be better spent testing, evaluating, and customizing Linux to meet the local team's computing needs rather than re-installing and configuring Windows every few months after the latest viruses swept through again. It continues to be used as the primary operating system of our partner organization in that location.

Since 2014 the main development of Wasta-Linux has continued from Ethiopia (እንኳን ደህና መጣ) and it has become the primary operating system supported by our organization in Ethiopia, with nearly 200 installations and counting.

Read more about the original motivations for Wasta-Linux in the ["case study" on our organization's move from Windows to Linux](/home/why-linux).
{{< /expand >}}

{{< expand "So, what is 'wasta' anyway?" >}}
<a href="https://en.wikipedia.org/wiki/Wasta" target="_blank"><b><i>"Wasta"</i></b></a> literally means "intermediary", but it implies more: it is seen as having "insider connections", or "special favor or ability to 'side-step the normal process.'" Think of needing to wait several days in the heat of a government office to get an official "stamp" on a piece of paper. If you have *wasta*, then you are able to come around through the "side door" and get the stamp immediately. So, Wasta-Linux is essentially "cutting to the front of the line" for new users to Linux in order to get a usable system without all the effort of starting from nothing. The analogy doesn't work when taken too literally, however: don't think there is anything unethical or illegal in the process! Wasta-Linux is just a light-hearted way to explain that you get the Linux you have been hoping exists without needing to hack on it to get it set up as you want!
{{< /expand >}}

{{< expand "How many Wasta-Linux users are there?" >}}
Great question! There are several locations using Wasta-Linux around the world, with some locations working in an offline-only environment. This means a single download could represent 10s of users or more. As of 2019, it seems clear that there are at least 500 Wasta-Linux users, but it could be multiples of that number.
{{< /expand >}}

{{< expand "How can Wasta-Linux be customized to meet my needs?" >}}
Beyond individual users that may find the Wasta-Linux system available here _"as-is"_ to fit them well in their situations, it is intended that Wasta-Linux can be used as a base for _"location specific customized versions"_ of Wasta-Linux (providing pre-installed location-specific fonts, keyboards, default applications, settings, reference documents and training materials, etc.). Once these "location specific customized Wasta-Linux versions" are made available, the ease of install of this customized Linux distribution will provide an opportunity for it to self-propagate throughout the region, even among low-tech computer users.

If customizing is of interest to you, please see this page:
[Wasta-Linux: Customizing for your needs](/home/customizing)
{{< /expand >}}
