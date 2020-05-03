# Dual Boot Ubuntu & Windows
Dual-Booting
: Two operating systems installed on a single PC

Dual booting works by splitting a hard drive with an existing operating system (OS) into multiple [**partitions**](https://www.howtogeek.com/184659/beginner-geek-hard-disk-partitions-explained/) and installing another OS into the newly created partition. Each partition is separate from the others and contained unless specially accessed. Once the computer is dual booting, a boot manager will allow the user to choose which OS to boot at each startup. It's also possible to boot from a portable OS on a portable memory drive with either the boot manager or your Basic Input Output System (BIOS). This guide will cover how to dual boot Windows and the recently released Ubuntu 20.04 LTS in the case where Windows is already installed.

* If you prefer to follow official documentation, here are the [Ubuntu Docs](https://help.ubuntu.com/community/WindowsDualBoot) describing the process. Please note these are dated and not comprehensive.
* If you wish to try Ubuntu before deciding to install, please see [Get Ubuntu](#get-ubuntu) for a bootable Ubuntu USB stick.

## Cost/Benefit
Pros
* Still have access to Windows for gaming or Windows only applications
* Get more out of your hardware, especially for old computers
* Separate Linux environment for work and separate Windows environment for general use
* Access to flexible & powerful Linux commands
* Big advantage to have Linux experience for future computer science education

Cons
* There may be some strange, trivial side effects which will require fixing eg. [discrepancy between Windows and Ubuntu clock](https://askubuntu.com/questions/169376/clock-time-is-off-on-dual-boot)
* Setting up dual booting can be dangerous for your machine if done incorrectly
* Takes up extra hard drive space

## Requirements
* $\ge$ 16 GB USB for a windows recovery drive
* Large USB or external hard drive for system backup
* Windows machine with free $\ge$ 25GB hard drive space
* $\ge$ 4 GB USB stick for Ubuntu Live
* About 3 free hours, dependant on speed of internet & the computer

## Steps
### 1. Back up Windows
#### Create a recovery disk
A recovery disk will allow you to reinstall windows, but not your files or apps, in case of a major problem. Microsoft has a great [walkthrough](https://support.microsoft.com/en-us/help/4026852/windows-create-a-recovery-drive) for this. Start by inserting your drive and search for `recovery drive`. Note that the process will erase any data previously on the USB.

#### Create a system image backup
A **system image** is a windows 7 feature that creates a perfect copy of partitions you select and is still available in later versions of windows. It can be used to do a complete recovery of windows and your file system. If you do not wish to keep your files, a USB recovery drive  may be all you need. The system image backup tool is accessible at `Control Panel --> System and Security --> Backup and Restore (Windows 7)`. The option will be listed in the panel on the left side. 

#### Recover your PC
You have recovery options in case something goes wrong. There are a couple useful recovery guides by [HowToGeek](https://www.howtogeek.com/239312/how-to-restore-system-image-backups-on-windows-7-8-and-10/)  and [Microsoft](https://support.microsoft.com/en-us/help/12415/windows-10-recovery-options). Window versions 7+ should come with a recovery environment ([winRE](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)), but you can check by typing `reagentc /info` on command prompt. You can use it to recover your OS and files with the system image you made. 

If you're able to boot, [Access winRE](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference#entry-points-into-winre) by holding shift while clicking the restart button. Then try some [](https://support.microsoft.com/en-us/help/4026030/how-to-use-windows-recovery-environment-winre-to-troubleshoot-common-s) to try to resolve any issues. 

If you can't boot at all, you'll have to use your recovery disk to boot. Follow the method in section [Install Ubuntu](#install-ubuntu) to boot from an external drive. Finally, find and select the `System Image Recovery` option in the and [recover your PC](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755163(v=ws.11)?redirectedfrom=MSDN) .

### 2. Get Ubuntu
A bootable Ubuntu USB stick is the easiest way to try or install Ubuntu. The official [guide](https://ubuntu.com/tutorials/tutorial-create-a-usb-stick-on-windows#1-overview) is very clear and thorough. ==flesh this out if extra time==

### 3. Install Ubuntu
Boot from the live Ubuntu USB by restarting your computer. [Access your BIOS settings](https://www.howtogeek.com/129815/beginner-geek-how-to-change-the-boot-order-in-your-computers-bios/) by pressing f2, del, esc or f12 during startup. The correct button is different between computers but it will be displayed on the manufacturer's startup screen. Choosing the `Minimal installation` option is recommended to avoid bloatware. Continue until the disk partitioning section.

### 4. Partitioning
Click on the `Manually edit partition table` option. ==repartition from ubuntu or windows?==

## Next Steps
* [Learn Linux basics](#linux_basics.md)
* [Setup Selkirk work environment](#work_environment)
