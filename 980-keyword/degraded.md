**(default: off)**

Allow mounts with less devices than the RAID profile constraints require. A read-write mount (or remount) may fail when there are too many devices missing, for example if a stripe member is completely missing from RAID0.

Since 4.14, the constraint checks have been improved and are verified on the chunk level, not at the device level. This allows degraded mounts of filesystems with mixed RAID profiles for data and metadata, even if the device number constraints would not be satisfied for some of the profiles.

Example: metadata -- raid1, data -- single, devices -- `/dev/sda`, `/dev/sdb`

Suppose the data are completely stored on _sda_, then missing _sdb_ will not prevent the mount, even if 1 missing device would normally prevent (any) _single_ profile to mount. In case some of the data chunks are stored on _sdb_, then the constraint of single/data is not satisfied and the filesystem cannot be mounted.