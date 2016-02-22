---
layout: post
title: Install Windows 7 From USB
---
This is a nifty little guide (code) for preparing your USB Drive to install Windows 7 on your PC i.e install windows 7 from USB drive. There are other ways of doing it but I think this is easy to write down and remember, no installing software that can disappear after a few years. 

**Windows Key + R**; write `cmd` then **Ctrl+ Shift+ Enter**  
`DISKPART`  
`LIST DISK`; choose an appropriate disk, either DISK 1 or DISK 2  
`SELECT DISK 1`  
`CLEAN`  
`CREATE PARTITION PRIMARY`  
`SELECT PARTITION 1`  
`ACTIVE`  
`FORMAT FS=NTFS`; Process may take some time, Go Grab some coffee.  
`ASSIGN`  
`EXIT`

`D: CD BOOT `; where **D: **is the drive you are copy from, either virtual drive or DVD drive.  
`CD BOOT `  
`BOOTSECT.EXE /NT60 H: `; where **H:** is your USB Drive.

Then copy your DVD files into the USB. Set BIOS priority to USB or better, when your PC is booting up, either hold F2, F8 OR F12. In Toshiba laptops, its mostly F12.

[Source][1]

 [1]: http://www.intowindows.com/how-to-install-windows-7vista-from-usb-drive-detailed-100-working-guide/
