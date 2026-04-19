# Backup Server Setup

Date Written: 19/04/2026 TODO: Update

## License

There are two licenses for this project. All code falls under the AGPLV3 license and all documentation/ write up falls under CC-BY-SA license.

I have no affiliation with any project mentioned in these write ups. I just like using the software.

## Who is this guide for

This guide is the path I took to setup a backup server for my Network Attached Storage (NAS). A [NAS setup Repo](https://github.com/EthanSousaProjects/Personal_Server_Setup) has been made, detailing what runs on the NAS and how I set it all up. Where relevant, this repo will refer to this repo as the service setup/ service details will be the same. Detailed setup will be in the NAS documentation repo. This guide is written from the perspective of someone who is somewhat tech literate with Linux and windows but by no means an expert. I am attempting to write these guides so that anyone somewhat tech literate can follow them. I acknowledge that not everyone will be able to follow these guides that i create due to a vast diversity of IT knowledge.

## The server

In this guide I am using an [Odroid HC4](https://www.hardkernel.com/shop/odroid-hc4/) from hardkernal. This is an ARM board just like a raspberry pi but, it is more specialized to a NAS setup. It contains SATA slots that can fit 2.5" and 3.5" drives. The [HC4 wiki](https://www.hardkernel.com/shop/odroid-hc4/) gives more information about the board if you are curious. In addition to the base board and power supply I have the following components:

- 1, 8TB SATA HDDs
- 1, 16GB Industrial Grade Micro SD card

## Guide Chapters

This guide is organized into Markdown chapters. Each chapter guides a part of the setup process. Having these chapters breaks down each step of the process into manageable chunks. The following list are the chapters in this guide (with links) with a brief description of what it is about:

1) [Installing OMV](01_Installing_OMV.md) - Installing the OS to the odroid HC4 with Open Media Vault.
2) [Rsync Setup](02_Rsync_Setup.md) - Setting up Rsync to pull data from the NAS.
3) TODO: Rsnapshot setup might not do this do to just 1 drive now. Rsnapshot on NAS side ideally i think for things like keepassdb. Have a good think about what.
4) TODO: Remote Backup server remote access setup (Zerotier)

## Repo setup

TODO: Write on how the repo is organized and link to the other md files with there titles for easy navigation. Slight explanation of each chapter and why it has been made.

TODO: Write on how VS codium is setup for this project.

TODO: Write on the extensions used to manage this repo through vs code/ codium.

TODO: Discuss spelling thing.
