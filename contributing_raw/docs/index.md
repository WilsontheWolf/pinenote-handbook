# Contributing to the PineNote Ecosystem

## Introduction

The software side of the PineNote is purely community driven.
It follows that all aspects of this software ecosystem need help, to varying
degrees.

In the following some long-standing themes are discussed. However, if you are
willing to actively help, please drop into the PineNote chat on
matrix/irc/telegram (see
[wiki.pine64.org](https://wiki.pine64.org/wiki/Main_Page#Chat_Platforms) ).

## What open issues are there?

This is mostly an documentation issue, and information is widely scattered
between the chat, the wiki, and the repositories containing the various parts
of the Debian image.  While in the end all general issues for the PineNote
should be collected and managed in the wiki, for now a first point of contact
is the issue tracker of the Debian image: https://github.com/PNDeb/pinenote-debian-image/issues
Here you will also find some meta issues that hopefully provide you with
enough information to tackle your issues, or find a place to contribute.

## Documentation

This is always an issue. User-side documentation can always use help. Usually
it's best if you try to contribute to this documentation by improving aspects
that you found difficult to follow, or topics that you think are important, but
are completely missing from the documentation.

Traditionally, technical, as well as user-focussed, information can be found in
the [Pine wiki](https://wiki.pine64.org/wiki/Main_Page).
However, the PineNote comes with a separate user manual (this document you are
reading right now), which resides in this GitHub
[repository](https://github.com/PNDeb/pinenote-handbook).

Issues and pull-requests are very welcome!

If you want to improve the technical documentation, it's best to focus on the
wiki (linked above).

## Upstreaming

There are ongoing efforts to get the missing pieces of the PineNote software
in the [mainline Linux kernel](https://en.wikipedia.org/wiki/Linux_kernel#Mainline_Linux)
and the [U-Boot](https://en.wikipedia.org/wiki/Das_U-Boot) boot loader.
This is a process known as upstreaming.
This includes the EBC kernel driver for the e-ink panel, various bugfixes and
other small improvements.  With everything upstreamed, the entire
[Device Tree](https://en.wikipedia.org/wiki/Devicetree) data for the PineNote,
all the required kernel drivers, complete boot loader support and the related
configuration will become part of the mainline Linux kernel and U-Boot, ensuring
that all Linux distributions can support the PineNote as a "first-class citizen".
This ensures that the PineNote will always support the latest available version
of the Linux kernel and U-Boot, preventing any kind of obsolescence in that regard.

If you want to help with these efforts or contribute in any way, please reach
out in the #pinenote channel on one of the
[community chat platforms](https://wiki.pine64.org/wiki/Main_Page#Chat_Platforms).

## Custom Software

# Kernel

The kernel currently used for the PineNote is maintained here:

https://github.com/m-weigand/linux

Look for branches beginning with "branch_pinenote_" to find ready-to-use
branches. Other branches contain individual patches for certain subsystems.

# Patched Debian Packages

Not many Debian packages need patching to get the PineNote running:

* **mesa** must be patched to allow 3D hardware acceleration in combination
  with the ebc driver.
* we use a slightly patched **gnome-shell** package to allow for better
  integration of certain ebc-related tasks. These are fully optional
  modifications.
