---
layout: post
title: Creating Bootable USB Drive Of Windows 11
subtitle: Any PC No TPM Installation
cover-img: img/posts/Win11/Firstlook1.jpg
thumbnail-img: /img/posts/Win11/Snap-feature.gif
share-img: img/posts/Win11/Firstlook1.jpg
tags: [Windows, Bootable]
---

Your device must be running Windows 10, version 2004 or later, to upgrade. Free updates are available through Windows Update in Settings>Update and Security.

- **Processor** 1 gigahertz (GHz) or faster with 2 or more cores on a compatible 64-bit processor or System on a Chip (SoC).

- **RAM** 4 gigabyte (GB).

- **Storage** 64 GB or larger storage device Note: See below under “More information on storage space to keep Windows 11 up-to-date” for more details.

- **System firmware UEFI, Secure Boot capable.** Check here for information on how your PC might be able to meet this requirement.

- **TPM Trusted Platform Module (TPM) version 2.0.** Check here for instructions on how your PC might be enabled to meet this requirement.

- **Graphics card** Compatible with DirectX 12 or later with WDDM 2.0 driver.

- **Display** High definition (720p) display that is greater than 9” diagonally, 8 bits per colour channel.

- **Internet connection and Microsoft account** Windows 11 Home edition requires internet connectivity and a Microsoft account. Switching a device out of Windows 11 Home in S mode also requires internet connectivity. Learn more about S mode here. For all Windows 11 editions, internet access is required to perform updates and to download and take advantage of some features. A Microsoft account is required for some features.

One of them is not available in your laptop or desktop Microsoft don’t allow to install windows on your device. 

But Here is method to install on unsupported devices. From this method you can upgrade Windows 10 to windows 11 or Can make Clean installation of windows 11.

![Win11](/img/posts/Win11/Snap-feature.gif)

Lets Begin,

### Preparations 

- Minimum 8Gib Flash drive 

- Media Creation tool of Windows 10 (Internet Required)

- Windows 11 ISO Image.

- Wimlib

Lets Begin Process,
#### Creating Windows 10 Bootable Pendrive.

Step 1 - Download Media Creation tool from Microsoft website.

![Win11](/img/posts/Win11/Win10-Media-2.png)

Step 2 - Run Downloaded Media creation tool
Step 3 - Click On accept
Step 4 - Click on Create Installation Media and Click on Next
![Win11](/img/posts/Win11/Media-installation-3.png)

Step 5 - UnCheck Recommanded option and choose 64bit windows 10 and Click on next.
![Win11](/img/posts/Win11/64bit-4.png)

Step 6 - Insert you flash drive to your device.
Step 7 - Choose USB Flash Drive Click on Next.
![Win11](/img/posts/Win11/usbflash-5.png)

Step 8 - Choose your USB Drive and Click on Next and wait It will download image and flash your drive 
        _Note:- (Time Depends upon your PC or Laptop hardware and Internet Speed)_
Step 9 - Click on Finish

#### Let’s Prepare Windows 11 ISO.

Step 1 - Go to your browser Search for windows 11 ISO on Microsoft 
![Win11](/img/posts/Win11/Windows11-6.png)

Step 2 - Go to the Bottom of the page and Choose windows 11 and click on Download

Step 3 - Choose Windows 11 Language, and Click on Conform.

Step 4 - Click on 64Bit Download, It will begin to download your windows 11 ISO.

### Preparing USB for windows 11

#### We Need Another Tool Called Wimlib 
Step 1 - Go to wimlib Website.
Step 2 - Choose wimlib zip file as per your windows architecture 
Step 3 - Extract zip file on desktop

#### Converting  Windows 10 Bootable Pendrive To Windows 11 

Step 1 - Go to your Pendrive Which your have just created for windows 10

Step 2 - Open Sources.

Step 3 - Look for install.wim and Delete it.

Step 4 - Go to your Windows 11 Downloaded location

Step 5 - Right click on windows 11 ISO and click on Mount _(It will mount windows 11 ISO on your Device)_

Step 6 - Open the folder of **wmlib** _(Which we have already downloaded and Extracted)_

Step 7 - Run Command Prompt and type cd Desktop and press enter

Step 8 - Type the command 

> wimlib-imagex.exe split f:\sources\install.wim e:\sources\install.swm 4000 

![Win11](/img/posts/Win11/Cmd-7.png)

> Note : Remember that f:\ is windows 11 mounted location and e:\ is windows 10 bootable pendrive location it’s different in your device 

And Press Enter Key, It wil take some time, when it will finish unmount your pendrive from your device. 

Here is ready your windows 11 Bootable USB Drive for Unsupported devices.




