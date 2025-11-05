+++
title = 'How to remove UEFI Partition from Windows'
date = '2025-10-02T04:11:12+05:30'
tags = ['windows', 'guide']
description = 'Delete an unwanted EFI System Partition from Windows using Diskpart.'
+++

1. Launch `Diskpart` from the run prompt press {{< kbd "⊞ Win" >}} + {{< kbd "R" >}}
2. List all the disk `list disk` - The drive number of the drive you want to delete from should be the same as it appears in the Disk Manager app.
3. Select the disk `sel disk [number of disk]` - where [Disk Number] is the number of the drive you want to delete from.
4. list all the partition of the selected disk `list partition`
5. select partition `sel partition [number of the partition]` - to choose the reserved partition you wish to delete.
6. Enter `delete partition override`

At this point, the EFI System Partition should be deleted. However, you should confirm by looking at the disk in the Windows Disk Management app.

If you need to remove the partition from BIOS/BOOT Menu, watch this video 

{{< linkicon "https://youtu.be/d06TUtD8IhI" "fa-brands fa-youtube" "Let's remove Ubuntu from Bios/Boot menu" >}}

> Source {{<linkicon "https://www.tomshardware.com/how-to/delete-efi-system-partition-windows" "fa-solid fa-blog" "Tom's Hardware Guide">}}
