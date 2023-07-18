---
#title: "Viết blog rất dễ dàng 👋."
#description: "Cái description này sẽ hiện ở /vn/blog."
#excerpt: "Hiện ở phần homepage blog."
date: 2023-07-14T09:19:42+01:00
lastmod: 2023-07-14T09:19:42+01:00
tags: ["DONE", "chattr", "lsattr"]
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
- "https://man7.org/linux/man-pages/man1/chattr.1.html"
Todo:
- a
- b
---
###### #InProgress  <progress value="18" max="100"></progress> 👍👍 Try harder 👍👍

```
lsattr file
---------------------m file
```
list attribute of file. **m** A file with the 'm' attribute is excluded from compression on file systems that support per-file compression.

#### ATTRIBUTES
**C**
A file with the 'C' attribute set will not be subject to copy-on-write updates. This flag is only supported on file systems which perform copy-on-write.
(Note: For btrfs, the 'C' flag should be set on new or empty files. 
if it is set on a file which already has data blocks, it is undefined when the blocks assigned to the file will be fully stable.
If the 'C' flag is set on a directory, it will have no effect on the directory, but new files created in that directory will have the No_COW attribute set. If the 'C' flag is set, then the 'c' flag cannot be
set.)



[read more attribute](https://man7.org/linux/man-pages/man1/chattr.1.html)