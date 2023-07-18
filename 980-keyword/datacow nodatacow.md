---
#title: "Viết blog rất dễ dàng 👋."
#description: "Cái description này sẽ hiện ở /vn/blog."
#excerpt: "Hiện ở phần homepage blog."
date: 2023-07-18T09:19:42+01:00
lastmod: 2023-07-18T09:19:42+01:00
tags: ["InProgress", "datacow", "nodatacow"]
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
- "https://btrfs.readthedocs.io/en/latest/btrfs-man5.html#man-btrfs5-mount-options"
Todo:
- a
- b
---
###### #InProgress18  <progress value="18" max="100"></progress> 👍👍 Try harder 👍👍

**(default: on)**

Enable data copy-on-write for newly created files. _Nodatacow_ implies _nodatasum_, and disables _compression_. All files created under _nodatacow_ are also set the NOCOW file attribute (see `chattr(1)`).

````ad-note
title: note
collapse: open

If _nodatacow_ or _nodatasum_ are enabled, compression is disabled.
````


Updates in-place improve performance for workloads that do frequent overwrites, at the cost of potential partial writes, in case the write is interrupted (system crash, device failure).