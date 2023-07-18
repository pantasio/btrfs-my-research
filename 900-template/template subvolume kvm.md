---
#title: "Viết blog rất dễ dàng 👋."
#description: "Cái description này sẽ hiện ở /vn/blog."
#excerpt: "Hiện ở phần homepage blog."
date: 2023-07-18T09:19:42+01:00
lastmod: 2023-07-18T09:19:42+01:00
tags: ["InProgress", "kvm", "subvolume"]
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


	sudo btrfs subvolume create /mnt/@kvm  
	sudo mount -o subvol=@kvm /dev/sdX /var/lib/libvirt  
	sudo vim /etc/fstab  
```
UUID=XXXX       /var/lib/libvirt/machines   btrfs   mount_options,subvol=@kvm   0 0 
```

![[Pasted image 20230718113229.png]]







