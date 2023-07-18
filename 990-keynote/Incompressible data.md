---
#title: "Viết blog rất dễ dàng 👋."
#description: "Cái description này sẽ hiện ở /vn/blog."
#excerpt: "Hiện ở phần homepage blog."
date: 2023-07-18T09:19:42+01:00
lastmod: 2023-07-18T09:19:42+01:00
tags: ["InProgress", "compression", "incompressible"]
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

Files with already compressed data or with data that won’t compress well with the CPU and memory constraints of the kernel implementations are using a simple decision logic. If the first portion of data being compressed is not smaller than the original, the compression of the file is disabled -- unless the filesystem is mounted with _compress-force_. In that case compression will always be attempted on the file only to be later discarded. This is not optimal and subject to optimizations and further development.

If a file is identified as incompressible, a flag is set (_NOCOMPRESS_) and it’s sticky. On that file compression won’t be performed unless forced. The flag can be also set by **chattr +m** (since e2fsprogs 1.46.2) or by properties with value _no_ or _none_. Empty value will reset it to the default that’s currently applicable on the mounted filesystem.

There are two ways to detect incompressible data:
- actual compression attempt - data are compressed, if the result is not smaller, it’s discarded, so this depends on the algorithm and level
- pre-compression heuristics - a quick statistical evaluation on the data is performed and based on the result either compression is performed or skipped, the NOCOMPRESS bit is not set just by the heuristic, only if the compression algorithm does not make an improvement

```
lsattr file
---------------------m file
```

Using the forcing compression is not recommended, the heuristics are supposed to decide that and compression algorithms internally detect incompressible data too.