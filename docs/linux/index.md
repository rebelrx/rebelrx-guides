# Linux

Guides for building clean, stable Linux setups for desktops, laptops, and servers.

This section focuses on practical installs, post-install configuration, and troubleshooting for light-weight Linux systems that DO NOT rely on systemd or any dystopic age/ID-verification infrastructure.

A full list of Linux distributions without systemd: [nosystemd.org](https://nosystemd.org/)

## Why No systemd?

Unfortunately, we are at the precipice of what most dysopian movies and stories warned about where our operating systems and core technological infrastructure will be turned into a surviellance/control system relying on ID-verification and social credit systems.

The entry point (beyond what is already established) will be the forced age/ID verification backbones embedded in the operating systems of all our electronic devices, including our desktop and mobile devices.

Most notably, all major operating systems including Micosoft Windows, Apple macOS, Apple iOS, and Google Android have already incorporated these ID-verification systems into their operating systems.

Linux, with it's open-source philosophy, was thought to be an alternative to these systems. However, that is now no longer true.

All operating systems require a primary initiliazation system (known as "init" in modern UNIX-based systems) which is the first process to boot after the system kernel is loaded into memory and is responsible for starting and managing core system services.

There are various types of init systems across different operating systems. Most modern Linux distributions now deploy an init known as "systemd," which for all of its issues, has already had its codebase updated by various bad actors in the Linux community to include age verification.

The only Linux distributions potentially left that would not be infused with age verification architecture, would be those that do not employ a systemd-based init.

I focus on 2 well known distributions without systemd that are forks of 2 of the most popular distros - Artix Linux, a non-systemd fork of Arch Linux, and Devuan, a non-systemd fork of Debian Linux.

## Guides

- [Artix Manual Install](artix-kde-openrc-install.md)
- [Devuan Server Install](devuan-server-install.md)

## Guides In Development

- Linux Terminal and Useful Commands Reference
