# Installation and Setup of unRAID

unRAID runs from USB flash drive.

* https://youtu.be/qwyx-TkGth0
* https://youtu.be/LmNNTFgKBBw
* https://youtu.be/QZcbig_iwrM

## TrueNas Core VS unRAID

* https://hardwarecanucks.com/forum/threads/truenas-core-vs-unraid.83621/

## Plugins

* Community Plugin https://raw.githubusercontent.com/Squidly271/community.applications/master/plugins/community.applications.plg

When the comminity plugin is installed you get a new tab called Apps. From there it's easy to
install other plugins then.

* Unassigned Devices
* Unassigned Devices Plus (Addon)

## Tutorials

* Turn an old PC into a powerful NAS solution using UNRAID! https://www.youtube.com/watch?v=r9n4hMFBqvo
* Easily move, copy and sync files to unRAID, within unRAID and from unRAID using Krusader: https://www.youtube.com/watch?v=I0XCFPAsWZE&t=232s
* How to setup and install the best plugins for unRAID: https://www.youtube.com/watch?v=1TTsV9nfazk
* Unraid: 20 Must Have Plugins (2021 Edition): https://www.youtube.com/watch?v=cZTWC_z9rKs

## Copy files from USB disk to unRAID

The unassigned disk will usually mount to /mnt/disks/ folder so if in the unraid gui you enter the console (top right) and do a

    $ cd /mnt/disks/
    $ ls

That should be your disk.  So for example if I have a folder called movies on my usb drive and a share called movies on my array, I want to copy from my usb drive to my array I would use this:

    cp -av /mnt/disks/WD_Book/Movies /mnt/user/Movies

copy files and directorys and list items copied from my usb drive to my movies directory on my array.

## Enable NFS

https://unraid.net/blog/deploying-an-unraid-nfs-server


## Enable array autostart

To enable the array to start automatically when the server is rebooted, go to the settings tab and click on Disk Settings. Then, where it says Enable auto start, change it to Yes, and then click on Apply. Now, anytime the server is rebooted, you won’t have to enable the array manually. It will be done automatically. Any Docker container and virtual machines will also start automatically after the array starts.

## Shutdown/Reboot

unraid stop the array before it proceeds to shut down