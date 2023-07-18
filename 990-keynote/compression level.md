---
#title: "Viết blog rất dễ dàng 👋."
#description: "Cái description này sẽ hiện ở /vn/blog."
#excerpt: "Hiện ở phần homepage blog."
date: 2023-07-14T09:19:42+01:00
lastmod: 2023-07-14T09:19:42+01:00
tags: ["InProgress", "compression", "level", "zlib", "zstd"]
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
###### #InProgress  <progress value="18" max="100"></progress> 👍👍 Try harder 👍👍


The level support of ZLIB has been added in v4.14, LZO does not support levels (the kernel implementation provides only one), ZSTD level support has been added in v5.1.

There are 9 levels of ZLIB supported (1 to 9): 
- mapping 1:1 from the mount option to the algorithm defined level.
- The default is level 3, which provides the reasonably good compression ratio and is still reasonably fast.
- The difference in compression gain of levels 7, 8 and 9 is comparable but the higher levels take longer.

The ZSTD support includes levels 1 to 15, a subset of full range of what ZSTD provides.
- Levels 1-3 are real-time, 
- Levels 4-8 slower with improved compression
- Levels 9-15 try even harder though the resulting **size may not be significantly improved**.

Level 0 always maps to the default. The compression level does not affect compatibility.