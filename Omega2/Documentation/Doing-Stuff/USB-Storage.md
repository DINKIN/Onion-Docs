---
title: USB Storage
layout: guide.hbs
columns: two
devices: [ Omega2 ]
order: 3
---

# Using USB Storage

// Explanation of how to use USB storage:

The Omega2 can read and write to USB storage devices, such as USB keys, and USB external hard-drives. This tutorial will show you how to expand the storage on your Omega2 using an external USB storage device.

## USB Storage and Linux

// Explanation of how a device needs to be mounted - make sure to highlight the Omega2 automounts USB storage, point out the location
On a linux device, a USB storage device needs to be mounted in order to be used. The Omega2 and Omega2+ come ready with an auto-mounting tool that will take care of that process for you! The default mount location is `/tmp/mounts/`. This can be changed by editing the config file located at `/etc/config/mountd`


## Using USB storage

// explanation of how to access files
Steps to access USB storage:

1. Plug in the USB Storage
2. Navigate to the correct directory
	* The default is `/tmp/mounts/`
		* `cd /tmp/mounts/`
3. Check the directory for your USB storage device
	* `ls`
		* Your device will usually be named `USB-A1`
		* `cd <device name>` to enter the storage space on your usb
			* In this example, this would be `cd USB-A1`
4.  Congratulations, you may now use your USB storage device for additional space on your Omega!

## Unmounting

// draw a parallel to safely disconnecting in Windows
Once you are done with your USB storage device, make sure you unmount your device to avoid corrupting your data.

The `umount` command is used to unmount the storage

```
umount <mount point>
```

From the above example:

```
umount /tmp/mounts/USB-A1
```

The USB device can now be safely unplugged.