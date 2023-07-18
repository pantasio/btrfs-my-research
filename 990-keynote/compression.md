---
#title: "Viết blog rất dễ dàng 👋."
#description: "Cái description này sẽ hiện ở /vn/blog."
#excerpt: "Hiện ở phần homepage blog."
date: 2023-07-14T09:19:42+01:00
lastmod: 2023-07-14T09:19:42+01:00
tags: ["InProgress", "compression", "hugo"]
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
- "https://btrfs.readthedocs.io/en/latest/Compression.html"
Todo:
- a
- b
---
###### #InProgress  <progress value="18" max="100"></progress> 👍👍 Try harder 👍👍

#### keynote 1

Once the compression is set, all newly written data will be compressed, i.e. existing data are untouched. Data are split into smaller chunks (128KiB) before compression to make random rewrites possible without a high performance hit. Due to the increased number of extents the metadata consumption is higher. The chunks are compressed in parallel.

#### keynote 2

Typically the compression can be enabled on the whole filesystem, specified for the mount point. Note that the compression mount options are shared among all mounts of the same filesystem, either bind mounts or subvolume mounts. Please refer to [btrfs(5)](https://btrfs.readthedocs.io/en/latest/btrfs-man5.html) section [MOUNT OPTIONS](https://btrfs.readthedocs.io/en/latest/btrfs-man5.html#man-btrfs5-mount-options).

	mount -o compress=zstd /dev/sdx /mnt

This will enable the `zstd` algorithm on **the default level (which is 3)**. The level can be specified manually too like `zstd:3`. **Higher levels compress better at the cost of time.** This in turn may cause **increased write latency**, low levels are suitable for real-time compression and on reasonably fast CPU don’t cause noticeable performance drops.














