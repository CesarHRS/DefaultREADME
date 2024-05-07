```markdown
<h1 align="center">Repository Name or Shortcut or Alias</h1>

<p align="center">
  <a href="https://img.shields.io/github/issues/ralvescosta/readme-template.svg">
    <img src="https://img.shields.io/github/issues/ralvescosta/readme-template.svg" alt="Issues">
  </a>
  <a href="https://img.shields.io/github/stars/ralvescosta/readme-template.svg">
    <img src="https://img.shields.io/github/stars/ralvescosta/readme-template.svg" alt="Starts">
  </a>
  <a href="https://img.shields.io/github/forks/ralvescosta/readme-template.svg">
    <img src="https://img.shields.io/github/forks/ralvescosta/readme-template.svg" alt="Forks">
  </a>
  <a href="https://github.com/ralvescosta/readme-template/actions/workflows/ci.yaml/badge.svg">
    <img src="https://github.com/ralvescosta/readme-template/actions/workflows/ci.yaml/badge.svg" alt="CI Action">
  </a>
</p>

Here you should put a brief summary of what's in this repository, why it's important, and explain a bit about how the problem was solved.

If there is a version of this readme in another language, please put the link here. Example:

English | [Portuguese](README-pt.md)

# Index

- [Repository Name](#repository-name)
- [Index](#index)
- [Prerequisites](#prerequisites)
    - [Linux (Debian)](#linux-debian)
    - [Linux (Arch)](#linux-arch)
    - [Windows (Chocolatey)](#windows-chocolatey)
    - [Windows (Installer)](#windows-installer)
- [Installation](#installation)
    - [Cloning the repository](#cloning-the-repository)
    - [Creating a build directory](#creating-a-build-directory)
    - [Compiling the program](#compiling-the-program)
- [How to Use the Program](#how-to-use-the-program)
    - [Firewall](#firewall)
- [Getting Started](#getting-started)
    - [Terminal Output](#terminal-output)
- [References](#references)

# Prerequisites

In this section, you'll explain what's needed and recommended to have installed beforehand to use the program.
Example:

<details><summary><b>Linux (Debian)</b></summary>

## Linux (Debian)

1. Install the python3 package:

    ```bash
    sudo apt install python3
    ```

</details><p>

<details><summary><b>Linux (Arch)</b></summary>

## Linux (Arch)

1. Install the python package:

    ```bash
    sudo pacman -S python
    ```

</details><p>

<details><summary><b>Windows (Chocolatey)</b></summary>

## Windows (Chocolatey)

1. Install the python package:

    ```shell
    choco install python
    ```

</details><p>


<details><summary><b>Windows (Installer)</b></summary>

## Windows (Installer)

1. Install python using the installer:

   To install python, you'll need to run the installer located on the [official python website](https://www.python.org/downloads/)

</details><p>

# Installation

In this section, you should start with the installation of the project itself. To keep the repository well-organized, you can also create various subsections breaking down the installation process into smaller parts to aid in better understanding of the process.

If any part of the installation is considered complex, adding images and GIFs can also help, especially when it's necessary to find a button in an interface or click through various settings in a menu following a specific order. 

Example:

<center>
 <img src="https://raw.githubusercontent.com/espressif/vscode-esp-idf-extension/master/media/tutorials/setup/install-extension.png" alt="Setup Wizard">
</center>

In the above image, you can easily understand what steps to follow and in what order, but it's good practice to explain the content in the image to ensure it's understood correctly.

> **WARNING:** Prefer adding images hosted on the internet to avoid cluttering the repository with image files. But if necessary, add an "images" folder, insert the images in this repository with the name in the following format: "1_image_name.png", and reference it in the readme relatively:

```markdown
![import_file](images/1_image_name.png)
```

<details><summary><b>Cloning the repository</b></summary>

First, you need to clone the repository, which can be done using the following command:

```bash
git clone (repository URL)
```

</details><p>


<details><summary><b>Creating a build directory</b></summary>

Below is an example demonstrating how to prepare the environment to compile an ANSI C application with cmake:

> **WARNING:** If the repository uses node.js, you might need to use the ``npm install`` or ``yarn install`` command. For these cases, modify this subsection accordingly.

Now, before running CMAKE, you need to create a folder called build and then change to that folder. This can be done using the following command:

```bash
mkdir build && cd build
```

</details><p>

<details><summary><b>Compiling the program</b></summary>

```bash
cmake ..
```

In some parts of the installation where common errors may occur, it's advisable to use a warning explaining how things might go wrong and common mistakes that can be made. Example:

> **WARNING:** Be careful not to run the MAKEFILE as a superuser, this can damage your operating system.

Another recommendation is to put a simple compilation table with the parameters you can use to compile the program, for example:

| Command    | Function                                                                   |
|------------|--------------------------------------------------------------------------|
| make clean | Deletes files created by the last compilation in the build folder         |
| make       | Compiles the program with the g++ compiler, the result is in the build folder |
| make run   | Compiles and then runs the program in the build folder                   |

</details><p>

# How to Use the Program

After installation, it's good to have a section to explain how to use the program as it was intended to be used, so explain what parameters it can receive, common inputs, and their expected outputs, etc. If necessary, you can also create a **Configuration** section to better explain how to configure the program. Depending on the program, it's possible to create another section just to explain what packet formats are used and examples of messages with them being sent.

Example:

<details><summary><b>Firewall</b></summary>

1. Firewall

    + Enable Firewall?
        - This helps protect your Mac from internet attacks.
    + Enable log?
        - If there's an infection, logs are useful for determining the source.
    + Enable stealth mode?
        - Your Mac won't respond to ICMP ping requests or connection attempts from closed TCP and UDP networks.

    2. General System Protection

        + Enable Gatekeeper?
            - Defend against malware by

 enforcing code signing and checking downloaded apps before allowing them to run.
        + Prevent automatic software whitelisting?
            - Both built-in and downloaded software will need user approval for whitelisting.
        + Disable Captive Portal Assistant and force login via browser on untrusted networks?
            - The Captive Portal Assistant could be triggered and redirect you to a malicious site WITHOUT any user interaction.

</details><p>

# Getting Started

The goal of this section is to go from the end of the compilation step to the first steps of running the program. In it, you'll show how the program should behave as a large part of the problems occur at this stage and it might be possible to identify if something went wrong. Below is an example output of version 3.4.0 of the esp32 firmware application running on a HG3 V1:

<details><summary><b>Terminal Output</b></summary>

```plain-text
rst:0x1 (POWERON_RESET),boot:0x12 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:2
load:0x3fff0030,len:1448
load:0x40078000,len:15548
ho 0 tail 12 room 4
load:0x40080400,len:4
0x40080400: _init at ??:?
load:0x40080404,len:3404
entry 0x40080614
I (586) cpu_start: Multicore app
I (595) cpu_start: Pro cpu start user code
I (595) cpu_start: cpu freq: 240000000 Hz
I (595) cpu_start: Application information:
I (598) cpu_start: App version:      v3.3.3-alpha.1-18-ga5895a91-dir
I (605) cpu_start: Compile time:     May  6 2024 10:44:14
I (611) cpu_start: ELF file SHA256:  6501359e6c327f1a...
I (617) cpu_start: ESP-IDF:          v5.2.1-dirty
I (622) cpu_start: Min chip rev:     v0.0
I (627) cpu_start: Max chip rev:     v3.99 
I (632) cpu_start: Chip rev:         v1.0
I (637) heap_init: Initializing. RAM available for dynamic allocation:
I (644) heap_init: At 3FFAE6E0 len 0000F480 (61 KiB): DRAM
I (650) heap_init: At 3FFCD098 len 00012F68 (75 KiB): DRAM
I (656) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (662) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (669) heap_init: At 40099388 len 00006C78 (27 KiB): IRAM
I (676) spi_flash: detected chip: generic
I (679) spi_flash: flash io: dio
I (684) coexist: coex firmware version: 77cd7f8
I (00:00:00.095) main_task: Started on CPU0
I (00:00:00.106) main_task: Calling app_main()
I (00:00:00.106) main: GTW Version: 3.4.0
I (00:00:00.109) main: GTW Hardware: HG3 V1
I (00:00:00.114) main: GTW Environment: prod
I (00:00:00.119) main: Heap: 242428
I (00:00:00.125) hg_app: Gateway Application Start
I (00:00:00.138) hg_flash: nvs initialized
I (00:00:00.139) gpio: GPIO[12]| InputEn: 1| OutputEn: 1| OpenDrain: 0| Pullup: 0| Pulldown: 0| Intr:0
I (00:00:00.143) gpio: GPIO[14]| InputEn: 1| OutputEn: 1| OpenDrain: 0| Pullup: 0| Pulldown: 0| Intr:0 
I (00:00:00.154) gpio: GPIO[35]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 0| Pulldown: 0| Intr:3
I (00:00:00.164) gpio: GPIO[4]| InputEn: 0| OutputEn: 1| OpenDrain: 0| Pullup: 0| Pulldown: 0| Intr:0
I (1797) wifi:wifi driver task: 3ffba5e4, prio:23, stack:6656, core=0
I (1797) wifi:wifi firmware version: a9f5b59
I (1797) wifi:wifi certification version: v7.0
I (1797) wifi:config NVS flash: enabled
I (1807) wifi:config nano formating: disabled
I (1807) wifi:Init data frame dynamic rx buffer num: 32
I (1807) wifi:Init static rx mgmt buffer num: 5
I (1817) wifi:Init management short buffer num: 32
I (1817) wifi:Init dynamic tx buffer num: 32
I (1827) wifi:Init static rx buffer size: 1600
I (1827) wifi:Init static rx buffer num: 10
I (1837) wifi:Init dynamic rx buffer num: 32
I (00:00:01.220) wifi_init: rx ba win: 6
I (00:00:01.224) wifi_init: tcpip mbox: 32
I (00:00:01.228) wifi_init: udp mbox: 6
I (00:00:01.233) wifi_init: tcp mbox: 6
I (00:00:01.237) wifi_init: tcp tx win: 5744
I (00:00:01.242) wifi_init: tcp rx win: 5744
I (00:00:01.247) wifi_init: tcp mss: 1440
I (00:00:01.252) wifi_init: WiFi IRAM OP enabled
I (00:00:01.257) wifi_init: WiFi RX IRAM OP enabled
I (1887) wifi:Set ps type: 0, coexist: 0
I (00:00:01.268) uart: queue free spaces: 

20
I (00:00:01.273) gpio: GPIO[17]| InputEn: 0| OutputEn: 1| OpenDrain: 0| Pullup: 0| Pulldown: 0| Intr:0 
I (00:00:01.282) uart: queue free spaces: 20
         (00:00:01.561) uart: queue free spaces: 20
I (00:00:01.562) hdr_bsc: BSC Exp/Recv Code date: 250923 / 250923
I (00:00:01.566) hg_http_server: Server Started on port 80
I (00:00:01.574) hg_settings: hg settings is corrupted. mac 
I (00:00:01.744) phy_init: phy_version 4791,2c4672b,Dec 20 2023,16:06:06
I (2427) wifi:mode : sta (78:21:84:66:5c:c0) + softAP (78:21:84:66:5c:c1)
I (2427) wifi:enable tsf
I (2437) wifi:Total power save buffer number: 16
I (2437) wifi:Init max length of beacon: 752/752
I (2437) wifi:Init max length of beacon: 752/752
I (00:00:01.829) hg_app: WIFI_EVENT_STA_START
I (00:00:01.833) esp_netif_lwip: DHCP server started on interface WIFI_AP_DEF with IP: 192.168.4.1
I (00:00:01.840) hg_app: WIFI_EVENT_AP_START
I (00:00:01.865) ksz80xx: auto detected phy KSZ8051/81/91
I (00:00:01.867) esp_eth.netif.netif_glue: 78:21:84:66:5c:c3
I (00:00:01.868) esp_eth.netif.netif_glue: ethernet attached to netif
I (00:00:05.866) hg_app: Ethernet Started
I (00:00:05.867) main_task: Returned from app_main()
I (00:00:07.867) hg_app: HG_APP_MSG_ID_RESET_TASK_WDT
I (00:00:09.867) hg_app: HG_APP_MSG_ID_RESET_TASK_WDT
I (00:00:11.867) hg_app: HG_APP_MSG_ID_RESET_TASK_WDT
I (00:00:13.867) hg_app: HG_APP_MSG_ID_RESET_TASK_WDT
```

</details><p>

# References

In this section, links to the APIs used in the repository will be placed, as well as a general explanation of the data structures used by the program.
