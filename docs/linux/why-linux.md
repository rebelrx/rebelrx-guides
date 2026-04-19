# 🐧 Why Linux

Most people don’t choose an operating system.

It is chosen *for them*.

* Windows → tied to Microsoft identity and telemetry
* macOS → tied to Apple’s ecosystem and hardware
* Mobile OS → fully locked, identity-bound platforms

Linux is different.

> Linux is the only major operating system that still allows you to opt out.

---

## 🧭 What This Page Covers

* Why Linux exists as an alternative
* What you gain (and what you give up)
* Key terms you need to understand
* What a Linux install actually looks like

---

## ⚔️ Why Choose Linux

### 🔐 Control

Linux gives you full authority over:

* Your system configuration
* Installed software
* Network behavior
* Update policies

No forced updates.
No mandatory accounts.
No hidden processes you cannot inspect.

> You are the administrator, not the vendor.

---

### 🧱 Transparency

Linux is open source.

That means:

* Code can be inspected
* Behavior can be verified
* Backdoors are harder to hide at scale

Compare that to:

* Windows → closed, opaque
* macOS → partially open, mostly controlled

---

### 🚫 No Forced Ecosystem

Modern operating system (OS) platforms are increasingly:

* Account-bound
* Cloud-dependent
* Identity-linked

Linux allows you to:

* Run fully offline systems
* Avoid account lock-in
* Use your machine without external validation

---

### ⚡ Efficiency

Linux systems are typically:

* Faster
* Less resource-intensive
* More stable over long periods

Especially when avoiding bloated defaults.

---

## ⚖️ The Tradeoff

Linux is not “free” in the way people think.

You are trading:

| Convenience        | Control        |
| ------------------ | -------------- |
| Plug-and-play apps | Manual setup   |
| Vendor support     | Self-reliance  |
| Familiar UX        | Learning curve |

> Linux rewards those willing to understand their system.

---

## 🧠 Core Concepts (Glossary)

Before installing Linux, you should understand a few key terms.

---

### 🧬 The Kernel

The kernel is the core of the operating system.

It sits between:

* Your hardware (CPU, RAM, disk, GPU)
* Your software (applications, services)

The Linux kernel is responsible for:

* Hardware communication
* Process management
* Memory management
* System security boundaries

> Everything in Linux ultimately runs through the kernel.

This is important because:

* All Linux distributions share the **same kernel foundation**
* The difference between distros is everything *around* the kernel

---

### 💻 CLI (Command Line Interface)

A text-based way to interact with your system. It's also known as the "terminal."

Instead of clicking:

* You type commands
* You control the system directly from a text-based terminal

Example:

```bash
ls
cd /home
cp file.txt backup.txt
```

All modern OS's ship with a built-in CLI. You may have not even known it was there in Windows or macOS!

On Windows, the CLI goes by a few names including:

* Terminal
* Command Prompt
* Windows Powershell

On macOS, the CLI is called Terminal.

However, Windows and macOS treat the CLI as optional and only for commanding advanced configurations.

Windows and macOS instead favor the graphical user interface (GUI) for everyday users (just **point and click**)

> The CLI is foundational for Linux and really not optional.

!!! tip "CLI Learning Curve (What to Expect)"

```
If you're coming from Windows or macOS, the CLI will feel uncomfortable at first.

This is normal.

Early on, you may find yourself:

- Copy/pasting commands you don’t fully understand  
- Searching for basic tasks (installing apps, navigating files)  
- Making small mistakes that break things temporarily  

This phase passes quickly.

Within a short time, the CLI becomes:

- Faster than point-and-click workflows  
- More precise and repeatable  
- A core advantage of using Linux  

> The goal is not to memorize commands, but to understand how the system works.
```

---

### 🐚 Shell (bash, zsh, etc.)

The shell is what interprets your commands.

Common shells:

* `bash` → default on most systems
* `zsh` → more customizable

Think of it as:

> The language you use to talk to your system within the CLI.

---

### 📦 Package Manager

The Package Manager is how Linux installs software.

Instead of downloading `.exe` files (like in Windows):

* You install from repositories

Examples:

* `apt` → Debian / Devuan
* `pacman` → Arch / Artix

Example command in Devuan to install the app, Nginx (used for web serving):

```bash
sudo apt install nginx
```

---

### 🧩 Distribution (Distro)

Distributions (or distros) are different “flavors” of Linux.

Each distro includes:

* Package manager
* Default tools
* System philosophy

Examples:

* Devuan → stable, server-focused, no systemd
* Artix → Arch-based, flexible, no systemd

> Linux is not just one OS; it is a family of systems.

---

### ⚙️ Init System

The system that starts everything at boot.

Examples:

* `systemd` → dominant, centralized
* `OpenRC`, `runit`, `s6` → simpler, modular

RebelRx Linux Guides prioritize:

> Non-systemd systems for greater transparency and control.

---

### 🗂️ Filesystem Structure

Linux does not use drive letters like `C:\`.

Instead:

* Everything is under `/` (root)

Examples:

* `/home` → user files
* `/etc` → system configs
* `/var` → logs and data

> Everything is a file, even devices.

---

### 🔐 Root vs User

* `root` → full system control
* `user` → limited access

You elevate privileges using:

```bash
sudo command
```

---

## 💻 Hardware Requirements

One of Linux’s biggest advantages:

> It runs on almost anything.

---

### 🧱 Minimum Reality

Linux can run on:

* Old laptops (10+ years old)
* Low-power mini PCs
* Servers
* Modern desktops and laptops

In many cases:

> Hardware that feels “slow” on Windows becomes fully usable again on Linux.

---

### ⚡ Modern Hardware

Linux also scales up:

* Multi-core CPUs
* High-end GPUs
* Large RAM configurations

However, compatibility depends on:

* GPU drivers (NVIDIA can require extra setup)
* Wi-Fi chipsets
* New or niche hardware

!!! warning "NVIDIA GPU Compatibility"

```
NVIDIA GPUs can require additional setup on Linux.

Unlike most hardware, NVIDIA drivers are not fully open source and often need:

- Manual driver installation  
- Matching driver versions with your kernel  
- Extra configuration for Wayland or desktop environments  

In contrast, AMD GPUs typically work out of the box with open-source drivers.

> If you are new to Linux, AMD hardware is generally the smoother experience.
```

---

### 🧠 Key Takeaway

* Windows and macOS are **hardware-constrained ecosystems**
* Linux is **hardware-flexible**

> You choose the hardware. Not the vendor.

---

## 🧩 Hardware Philosophy (Framework Recommendation)

If you’re buying new hardware, choose vendors aligned with Linux principles.

### 🔧 Framework Computer

Framework is one of the few companies that aligns with:

* Right-to-repair
* Modular hardware design
* Linux compatibility

Framework systems allow you to:

* Replace components instead of replacing the entire device
* Upgrade over time
* No forced hardware obsolescence

> Your hardware should be as sovereign as your software.

👉 Check out Framework laptops and desktop: <https://frame.work/>

---

## 🛠️ What a Linux Install Actually Looks Like

Installing Linux is fundamentally different from Windows or macOS.

---

### 🧱 Windows / macOS

* Boot installer
* Click through GUI
* System auto-configures
* Account required
* Done

---

### 🐧 Linux (Typical Flow)

Depending on distro, expect:

1. Boot into a live environment
2. Partition disks manually (or semi-manually)
3. Install base system
4. Configure:

   * Users
   * Networking
   * Bootloader
5. Install desktop environment (if needed)
6. Reboot into your system

!!! warning "Disk Partitioning Risk"

```
Linux installs often require manual disk partitioning.

This is one of the few steps where you can accidentally:

- Delete existing data  
- Overwrite another operating system  
- Misconfigure your boot setup  

Always:

- Back up important data before installing  
- Double-check selected disks and partitions  
- Understand whether you are replacing or dual-booting  

> Partitioning is powerful—but it assumes you know what you're doing.
```

---

### 🔧 Post-Install Reality

After install, you are not “done.”

You will:

* Install core software
* Configure services
* Set up networking and firewall
* Tune performance and usability

> Linux is built, not handed to you.

---

## 🧭 Who Linux Is For

Linux is a strong fit if you:

* Value privacy and independence
* Want full control over your system
* Are willing to learn and troubleshoot
* Prefer long-term stability over convenience

---

## 🚫 Who It’s Not For

Linux may frustrate you if you:

* Expect plug-and-play everything
* Rely heavily on proprietary software (Microsoft 365, Adobe, etc.)
* Want zero maintenance or learning

---

## 🧠 Final Thought

Most operating systems are moving toward:

* Identity enforcement
* Platform control
* Reduced user autonomy

Linux is one of the last environments where:

> The user is still in charge.

But only if you choose it intentionally.

---

## ➡️ Next Step

If this aligns with your goals:

* Start with a guided install
* Accept the learning curve
* Build your system deliberately

👉 Continue to:

* [Artix Desktop Manual Install](artix-kde-openrc-install.md)
* [Devuan Server Install](devuan-server-install.md)
