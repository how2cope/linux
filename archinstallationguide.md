# Arch Linux Installation Guide
### …including LUKS/dm-crypt setup for encrypted system drive, wow!

![img1](img/img1.png "img1")


## Preparing a bootable USB install medium

Follow the instructions on the Arch Wiki:
[https://wiki.archlinux.org/index.php/USB_flash_installation_media](https://wiki.archlinux.org/index.php/USB_flash_installation_media)



## Booting into the live installation media
You can boot into the USB you've just created.
Specify boot settings in the BIOS of your system, or select the boot device during startup.

List your available disks with

```
lsblk
```

Determine which device you want to use to install Arch Linux on. This is the drive we'll be using during this guide.

Now open we gdisk to create a GPT partition table and a boot and system partition. (reference: [man page for gdisk](https://www.commandlinux.com/man-page/man8/gdisk.8.html]))
```
gdisk /dev/<yourdiskhere>
```
for example:
```
gdisk /dev/sdb
```

This will open gdisk for the specified device.
