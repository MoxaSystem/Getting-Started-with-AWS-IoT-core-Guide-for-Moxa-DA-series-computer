# Getting Started with AWS IoT core Guide  for Moxa DA series computer

# Document Information

## Revision History (Version, Date, Description of change)

| Version | Date        | Description of change |
| ------- | ----------- | --------------------- |
| 1       | 2021//04/19 | First release         |
|         |             |                       |

# Overview

Moxa industrial-grade, fanless x86 computers have passed rigorous tests and strictly adhere to rigorous industrial standards to ensure they can provide long-lasting, reliable operation even in harsh environments, making them perfect for heavy industry, power substation and utilities, transportation, oil and gas, and maritime applications.

For more information, visit [Moxa X86-based Computers portal site](https://www.moxa.com/en/products/industrial-computing/x86-computers).

# Hardware Description

## DataSheet

Please based on the product series you purchased, click the link below accordingly.

[**DA-681C Series**](https://www.moxa.com/getmedia/baf0f371-534f-4a9f-949c-3d00c88509e1/moxa-da-681c-series-datasheet-v1.3.pdf)

[**DA-682C Series**](https://www.moxa.com/getmedia/d7ce4160-6bf7-441f-ba60-aa1f6bbd9f0c/moxa-da-682c-series-datasheet-v1.4.pdf)

[**DA-820C Series**](https://www.moxa.com/getmedia/1b593e53-2a27-4669-b897-b17e0e6b7b86/moxa-da-820c-series-datasheet-v1.7.pdf)

[**DA-720 Series**](https://www.moxa.com/getmedia/d4b87b2d-8dfa-47fa-8c37-d2dc2eda1db8/moxa-da-720-series-datasheet-v1.3.pdf)

For more information, visit Moxa [Substation Automation](https://www.moxa.com/en/solutions/power) portal site.

## Standard Kit Contents

The standard shipping Moxa DA series computer package contains the following items:

- 1 x DA-681C/DA-682C/DA-820C/DA-720 rackmount computer
- 1 x Rack-mounting kit
- 1 x Quick installation guide (printed)
- 1 x Warranty card

## User Provided items

To setup and operate Moxa computer, users have to prepare the following items by themselves.

- 10/100M Ethernet cable
- 100 to 240 VAC, 110 to 240 VDC

## 3rd Party purchasable items

N/A

# Set up your hardware

- **Connecting a Display**

    Moxa DA series computer comes with VGA/HDMI interfaces on the rear panel. Connect a display monitor to the VGA/HDMI interfaces.

- **Connecting a Keyboard and Mouse**

    Connectors for a keyboard and mouse are located on the rear panel of the computer. Both connectors are USB interfaces; you can directly connect a keyboard and a mouse using these connectors.

- **Powering on Moxa DA series computer :**

    These models provides dual power inputs using a terminal block, which is located on the rear panel. Connect the power cord wires to the screws, and then tighten the screws. The Power LED will light up to indicate that power is being supplied to them, after which the BIOS will initialize the flash disk module, causing the Storage LED to blink. Please based on the product series you purchased choose pin assignments accordingly. The VAC/VDC pin assignments are show in the figure.

    **DA-681C/DA-682C/DA-820C:**

    ![images/Untitled.png](images/Untitled.png)

    **DA-720:**

    ![images/Untitled%201.png](images/Untitled%201.png)

    ![images/Untitled%202.png](images/Untitled%202.png)

It takes around 30 to 60 seconds for the system to boot up.

- **Accessing Moxa DA series computer Using a Linux/Windows PC or Mac**

    You can use a PC to access Moxa DA series ****computer by using SSH over the network. Refer to the following IP addresses and login information:

    ![images/image2.png](images/image2.png)

Login: moxa

Password: moxa

Root account login is disabled until you manually create a password for the account. The user moxa is in the sudo group so you can operate system level commands with this user using the sudo command.

**ATTENTION: For security reasons, we recommend that you disable the default user account and create your own user accounts or** 

**Refer to Account Management of [Moxa DA series computer-linux-user-manual](https://www.moxa.com/getmedia/1b74d195-7939-4697-ae99-714b00478b5b/moxa-da-820c-series-linux-manual-v1.0.pdf) for the detail steps.**

- **Change the network settings of Moxa DA series computer based on your network environment**

    Refer to the Changing the interfaces Configuration File of [Moxa DA series computer-linux-user-manual](https://www.moxa.com/getmedia/1b74d195-7939-4697-ae99-714b00478b5b/moxa-da-820c-series-linux-manual-v1.0.pdf) for the detail steps.

# Set up your Development Environment

## Tools Installation (IDEs, Toolchains, SDKs)

The operation system of Moxa DA series is a native 64-bits X86 Linux operating system. There is no need to install toolchains. You can install development tools in Moxa DA series computer directly.

Follow these steps to update the package menu:

1. Make sure a network connection is available.

2. Use apt-get update to update the Debian package list.

```bash
moxa@Moxa:~$ sudo apt-get update
```

3. Install the native compiler and necessary packages.

```bash
moxa@Moxa:~$ sudo apt-get install gcc build-essential flex bison automake
```

# Setup your AWS account and Permissions

Refer to the instructions at [Set up your AWS Account](https://docs.aws.amazon.com/iot/latest/developerguide/setting-up.html). Follow the steps outlined in these sections to create your account and a user and get started:

- Sign up for an AWS account and
- Create a user and grant permissions.
- Open the AWS IoT console

Pay special attention to the Notes.

# Create Resources in AWS IoT

Refer to the instructions at [Create AWS IoT Resources](https://docs.aws.amazon.com/iot/latest/developerguide/create-iot-resources.html). Follow the steps outlined in these sections to provision resources for your Moxa DA series computer:

- Create an AWS IoT Policy
- Create a thing object

Pay special attention to the Notes.

> **Important**
Before you continue to the next step, your Moxa computer must be configured, and running. The Moxa computer must be connected to the Internet and you will need to be able to access the computer by using its command line interface. Command line access can be through SSH terminal remote interface.

# Build the demo

Follow above section, **Accessing Moxa DA series** **computer Using a Linux/Windows PC or Mac,** using PuTTY to open a remote terminal to Moxa computer on **Linux/Windows PC or Mac** and perform the following instructions in that window. 

Refer to the instruction at [Install the required tools and libraries for the AWS IoT Device SDK](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-sdk-tools) and [Install AWS IoT Device SDK](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-install-sdk) for Python on Moxa DA series computer directly. Follow the steps outlined in these sections to install AWS IoT Device SDK for your Moxa computer:

- Update the operating system and install required libraries
- Install git
- Install the AWS IoT Device SDK for Python.

Note: Due to using Python, there is no need to compile/build any programs. And we perform all steps in Moxa computer, there is no need to load/upload any programs to it.

# Run the demo

Continue previous section, perform the instructions, [Install and run the sample app](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-node-app-run), in that terminal window. 

To view the MQTT messages published by the sample app in the AWS IoT console, perform the instructions,[View messages from the sample app in the AWS IoT console](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-view-msg).

# Debugging

1. Not able to login Moxa DA series computer's through SSH terminal.

    Connect a display monitor to the Moxa DA series computer, and then power it up. Once the system is ready, a login screen will appear on your monitor. Refer to Starting from a VGA Console of [**Moxa DA series computer-linux-user-manual](https://www.moxa.com/getmedia/1b74d195-7939-4697-ae99-714b00478b5b/moxa-da-820c-series-linux-manual-v1.0.pdf)** for the detail steps. After login Moxa computer check following items:

    a. Check if IP address of LAN1/LAN2 is in the same subnet of your PC.

    b. Check if you are able to operate OS normally. If not, gather all error message when you operate OS and then [CONTACT US](https://www.moxa.com/en/support/technical-support)

2. Moxa computer is not able to access internet.

    a. Check if IP address, mask and gateway of LAN1/LAN2 are configured in /etc/network/interfaces properly.

    b. Check if routing is correct.

    c. Check if nameserver is configured in /etc/resolv.conf

# Troubleshooting

Still need assistance with your Moxa product? [CONTACT US](https://www.moxa.com/en/support/technical-support)
