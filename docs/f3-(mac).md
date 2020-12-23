---
title: "F3 (Mac)"
---

{% include toc title="Table of Contents" %}

### Required Reading

This is an add-on section for checking your SD card for errors using F3.

Depending on the size of your SD card and the speed of your computer, this process can take up to several hours!

This page is for Mac users only. If you are not on Mac, check out the [H2testw (windows)](h2testw-(windows)) or [F3 (Linux)](f3-(linux)) pages.

### What You Need

* [F3](assets/f3mac.zip)

### Instructions

1. Unzip the F3 `.zip` file
1. Move the `f3` folder to the Desktop
1. Insert your SD card into your computer
1. Open Terminal
1. Type `cd ~/Desktop/f3`
1. Type `./f3write /Volumes/<sd card name here>/`
1. Wait until the process is complete. See below for an example output.

~~~ bash
$ ./f3write /Volumes/SDCARD/
Free space: 29.71 GB
Creating file 1.h2w ... OK!
...
Creating file 30.h2w ... OK!
Free space: 0.00 Byte
Average Writing speed: 4.90 MB/s
~~~

1. Type `./f3read /Volumes/<sd card name here>/`
1. Wait until the process is complete. See below for an example output.

~~~ bash
$ ./f3read /Volumes/SDCARD/
									SECTORS      ok/corrupted/changed/overwritten
Validating file 1.h2w ... 2097152/        0/      0/      0
...
Validating file 30.h2w ... 1491904/        0/      0/      0

	Data OK: 29.71 GB (62309312 sectors)
Data LOST: 0.00 Byte (0 sectors)
					Corrupted: 0.00 Byte (0 sectors)
	Slightly changed: 0.00 Byte (0 sectors)
				Overwritten: 0.00 Byte (0 sectors)
Average Reading speed: 9.42 MB/s
~~~

___

If the test shows the result `Data LOST: 0.00 Byte (0 sectors)`, your SD card is good and you can delete all `.h2w` files on your SD card
{: .notice--success}

If the test shows any other results, your SD card may be corrupted or damaged and you may have to replace it!
{: .notice--danger}

### Return to [Get Started](get-started)
{: .notice--primary}
