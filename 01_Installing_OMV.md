# Installing Open Media Vault

Date Written: 25/02/2026 TODO: Update

This guide outlines the process of installing Open Media Vault (OMV) on the Odroid HC4 specifically. It must be noted that at the time of writing. There are many ways to install OMV depending on platform (X86 PC, Raspberry Pi, etc). This guide will go over the specifics of installing OMV on the HC4. Please research the process for your appropriate platform. You can view my [NAS Setup guide](https://github.com/EthanSousaProjects/Personal_Server_Setup) which uses an X86 Pc for installing OMV. Further details of this method and others can be found in the [OMV installation documentation page](https://docs.openmediavault.org/en/latest/installation/index.html).

## SD card Image flashing

To install OMV on this board, we need to flash the boot SSD and remove the default Petitboot loader. This loader is installed by default on this odroid board and we must remove it to allow the board to correctly boot. The [Armbian HC4 page](https://www.armbian.com/odroid-hc4/) describes how to remove the petitboot loader. It has been included here for completeness.

1) Connect a monitor and keyboard to the board and power it up.
2) Once booted up, in the Petitboot menu, go to `exit to shell`.
3) Once in the shell, run the following commands

```sh
flash_eraseall /dev/mtd0
flash_eraseall /dev/mtd1
flash_eraseall /dev/mtd2
flash_eraseall /dev/mtd3
```

Once completed, you are ready to install armbian to an SD card.

The easiest method to flashing the armbian image to the SD card is to use [Armbian Imager](https://github.com/armbian/imager). This is a flashing utility built for the armbian project making it easy to flash the correct board image to an SD card. I would recommend this method to users new to the process. I however, will install my image through [raspberry pi imager](https://www.raspberrypi.com/software/) downloading the correct image from the [Armbian HC4 page](https://www.armbian.com/odroid-hc4/) and verifying the file integrity and authenticity. An alternative to raspberry pi imager is [BalenaEtcher](https://etcher.balena.io/) which is commonly used. My [NAS OMV install guide](https://github.com/EthanSousaProjects/Personal_Server_Setup/blob/main/01_Installing_OMV.md) uses BalenaEtcher.

How to verify the file Integrity and authenticity in detail will not be mentioned in this repo. Please read through my [NAS OMV install guide](https://github.com/EthanSousaProjects/Personal_Server_Setup/blob/main/01_Installing_OMV.md) for details on checking the file integrity. The [Armbian getting started guide](https://docs.armbian.com/User-Guide_Getting-Started/#how-to-check-download-authenticity) also details how to do this. A simple file integrity check on linux and mac can be done via the command `sha256sum -c <image file name>` when both the sha256 and image are in the same folder/ directory. Please make sure which ever file you download is the armbian application image for OMV found on the [Armbian HC4 page](https://www.armbian.com/odroid-hc4/).

Once the file has been downloaded and verified, connect your SD card to your computer and launch the raspberry pi imager. As this imager is built around expecting to flash an SD card for a raspberry pi, we have to do something odd to get it to work. In the first left most option, where it asks you to select a `Raspberry Pi Device`, select the `No filtering Option`. This will allow you to select your own ISO file in the `Operating System` option in the middle. After that, select the appropriate SD card connected. Once all those options are selected, it should look like the image bellow.

![Raspberry Pi imager full options](Installing_OMV/Imager_Full_Setup.png)

Click the `NEXT` button when ready. You will be asked about using custom options. Select the `No` option. The SD card will now be getting flashed with our image. Wait for the finish prompt and remove it from the computer.

You have now flashed the SD card for the HC4. Now install it into the board.

## First Boot

When first booting up the server there are a few things we need to setup. You could connect to the server via a keyboard and monitor or through SSH. This guide will go over the SSH route.

The first step for logging into the server via SSH is to find the servers IP address. There are many ways to do this but, the most common is to login to your router and find the sever entry in the DHCP table.

## Drive setup

TODO: finish bit and talk about setting static IP address and/ or DHCP

TODO: Write basic Install guide

TODO: Add link about more OMV details to NAS repo as more detailed. Keep this basic.

TODO: Consider Drive setup to be separate chapter depending on how large this chapter gets.
