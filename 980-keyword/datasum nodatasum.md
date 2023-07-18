---
#title: "Viết blog rất dễ dàng 👋."
#description: "Cái description này sẽ hiện ở /vn/blog."
#excerpt: "Hiện ở phần homepage blog."
date: 2023-07-18T09:19:42+01:00
lastmod: 2023-07-18T09:19:42+01:00
tags: ["InProgress", "datasum", "nodatasum"]
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
###### #InProgress18 <progress value="18" max="100"></progress> 👍👍 Try harder 👍👍

**(default: on)**

Enable data checksumming for newly created files. _Datasum_ implies _datacow_, i.e. the normal mode of operation. All files created under _nodatasum_ inherit the “no checksums” property, however there’s no corresponding file attribute (see `chattr(1)`).

````ad-note
title: note
collapse: open

If _nodatacow_ or _nodatasum_ are enabled, compression is disabled.
````
There is a slight performance gain when checksums are turned off, the corresponding metadata blocks holding the checksums do not need to updated. The cost of checksumming of the blocks in memory is much lower than the IO, modern CPUs feature hardware support of the checksumming algorithm.
