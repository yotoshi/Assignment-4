# Assignment-4

This is my 4th assignment for this class. I have chosen the first option so I can use my past experiences with Lineage (my older phone was running on Lineage OS 14.0 and Cyanogen OS before that) to the Rpi.
To achieve this assignment I have used the KonstaKang build of Lineage 16.0 (Android 9) for Rpi and OpenGAPPS to install the Google services.
In order to cross-compile this build, I used Oracle VM machine running Ubuntu 18.4.
Unfortunately, the Rpi 4B is not powerful enough to run smoothly on this build. I have tried overclocking it but my cooling hardware system was not powerful enough to run it stable.
I have also attached some running screen capture of the process.

First, I have clean and format my SD Card using this tool:
[https://www.sdcard.org/downloads/formatter/]

Then, I have downloaded the image of Lineage (I could not attached it with git because of the file size)
[https://androidfilehost.com/?fid=4349826312261721851]
You need to unzip the file in order to use it

I also have dowload the OpenGAPPS according to this build
[https://opengapps.org/]
(Choose arm 9.0 pico)
This is the minimum required to get the Google services running.

To build Android into the Rpi, I have followed this guide provided by the Rpi website:
[https://www.raspberrypi.org/documentation/installation/installing-images/linux.md]

- Run lsblk -p to see which devices are currently connected to your machine.
- Check the SD card name (should be something like sdbX) X should be replaced by a letter depending on how many usb periphericals are plugged in
- If any partitions on the SD card have been mounted, unmount them all with umount, for example umount /dev/sdX1 (replace sdX1 with your SD card's device name, and change the number for any other partitions).
- Then run the following command
	dd bs=4M if=**lineage-16.0-20200212-UNOFFICIAL-KonstaKANG-rpi4.zip** of=/dev/**sdX** status=progress conv=sync
	(Replace the emphized part by the path to your .img file and the name of your SD Card)


I have followed this video in my attempt to OC the Rpi
[https://www.youtube.com/watch?v=TwDbQ26_Mp8]





