---
#title: "Viết blog rất dễ dàng 👋."
#description: "Cái description này sẽ hiện ở /vn/blog."
#excerpt: "Hiện ở phần homepage blog."
date: 2023-07-18T09:19:42+01:00
lastmod: 2023-07-18T09:19:42+01:00
tags: ["InProgress", "subvolume", "hugo"]
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

### mariadb

	/var/lib/mariadb

	sudo mount /dev/sdX /mnt
	sudo btrfs subvolume create /mnt/@mariadb
	sudo mount -o subvol=@mariadb /dev/sdX /var/lib/mariadb