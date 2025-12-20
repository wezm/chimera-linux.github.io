---
title: New images
layout: post
excerpt_separator: <!--more-->
---

The 20251220 set of images is now published.

This is an incremental refresh.

<!--more-->

## Changes

This set has been overdue for a while so it mainly comes as
an update with new versions.

This set is based on kernel 6.18 and comes with latest versions
of desktop environments and most other software.

Newly, the live images will not automatically import LVMs and
ZFS pools, as that was found to be unintuitive and sometimes
system-breaking (with ZFS-on-root setups).

Additionally, the images now come with an experimental TUI
installer. It can be invoked as `chimera-installer` from the
command line.

The installer supports the following:

* Local and remote installs
* APK mirror setup, with up to date mirror list fetched from the repo
* Basic setup (hostname, timezone, root password, user account)
* Installing extra packages
* Kernel version selection
* Bootloader setup (GRUB and systemd-boot, including BIOS/EFI/OF)

It does not support the following:

* Disk partitioning and formatting
* And probably a lot of other things

You are expected to partition, format, and mount your filesystem
layout beforehand and then point the installer to the mounted root.
This is by design and will remain that way, however a separate tool
for simplified disk setup may be provided later on.

However, it does validate your mounted filesystem tree for baseline
correctness, performs detection of system-specific things (like ESP)
and automatically generates `crypttab` for encrypted setups (this is
rudimentary so if you use keyfiles or other advanced things you need
to tweak it afterwards).

## Next images

The next set will come early next year with some more major changes.
