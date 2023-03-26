# Better File System
## A highly reliable modern file system

* BTRFS is a relatively new file system used on some major linux distrobutions.
* It is a copy on write system, meaning all changes are copied and can be snapshotted.
* Uses subvolumes rather than partitioning.
* Uses Checksums to identify data corruption or loss.
* RAID is built in ( However avoid RAID as it is still in development ).