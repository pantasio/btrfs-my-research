---
#title: "Viết blog rất dễ dàng 👋."
#description: "Cái description này sẽ hiện ở /vn/blog."
#excerpt: "Hiện ở phần homepage blog."
date: 2023-07-18T09:19:42+01:00
lastmod: 2023-07-18T09:19:42+01:00
tags: ["InProgress", "device", "devicepath"]
categories: ["Obsidian"]
contributors: ["Pantasio"]
readingTime: 15
pinned: false
$homepage: false
# this image for hugo blog, how to port Obsidian to hugo????
#images: ["kris-mikael-krister-aGihPIbrtVE-unsplash.jpg"]
#draft: false
#weight: 40
aliases:
ChangeLog: 
Original-post:
- "https://pantasio.com"
Todo:
- a
- b
---
###### #InProgress18  <progress value="18" max="100"></progress> 👍👍 Try harder 👍👍

Specify a path to a device that will be scanned for BTRFS filesystem during mount. This is usually done automatically by a device manager (like udev) or using the **btrfs device scan** command (e.g. run from the initial ramdisk). In cases where this is not possible the _device_ mount option can help.

````ad-note
title: note
collapse: close

Booting e.g. a RAID1 system may fail even if all filesystem’s _device_ paths are provided as the actual device nodes may not be discovered by the system at that point.
````
