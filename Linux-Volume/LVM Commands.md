
# LVM and Disk Management Commands

This document provides a guide to using Linux commands for LVM (Logical Volume Management) and disk management.

## Commands Overview

```bash
lsblk
clear
vgs
lvs
mkdir /mnt/sam_lv_mount
mkfs.ext4 /dev/test_vg/demo_lv
mount /dev/test_vg/demo_lv /mnt/sam_lv_mount
cd /mnt/sam_lv_mount/
mkdir devops
vim demo.txt
cd
cat /mnt/sam_lv_mount/devops/demo.txt
umount /mnt/sam_lv_mount/
mount /dev/test_vg/demo_lv /mnt/sam_lv_mount
mkdir /mnt/sam_disk_mount
mkfs -t ext4 /dev/xvdh
mount /dev/xvdh /mnt/sam_disk_mount/
df -h
```

## Description of Commands

1. **lsblk**: Lists all block devices in a tree format to display their relationships.
2. **clear**: Clears the terminal screen for better readability.
3. **vgs**: Displays information about the volume groups.
4. **lvs**: Lists logical volumes in the system.
5. **mkdir**: Creates a directory, used here for mounting logical volumes and disks.
6. **mkfs.ext4**: Formats the specified device or logical volume with the ext4 filesystem.
7. **mount**: Mounts a filesystem (logical volume or block device) to the specified directory.
8. **cd**: Changes the current working directory.
9. **vim**: Opens the Vim editor to create or edit files.
10. **cat**: Outputs the content of a file to the terminal.
11. **umount**: Unmounts a filesystem from a directory.
12. **df -h**: Displays disk usage and available space in a human-readable format.

## Workflow Example

1. Create and format a logical volume (`/dev/test_vg/demo_lv`) with ext4 and mount it to `/mnt/sam_lv_mount`.
2. Create a directory named `devops` and add a text file using `vim`.
3. Verify the contents of the file with `cat` after mounting and unmounting the logical volume.
4. Format the block device (`/dev/xvdh`) with ext4 and mount it to `/mnt/sam_disk_mount`.
5. Use `df -h` to check disk space usage and confirm the mounts.

---

## Notes

- Ensure you have the necessary administrative privileges (e.g., root or sudo) to execute these commands.
- Always unmount devices before removing or making significant changes to the underlying filesystem.

