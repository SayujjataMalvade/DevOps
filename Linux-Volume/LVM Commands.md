# EC2 SSH Connection and Disk Management on Linux

This repository provides step-by-step instructions for:

1. Establishing SSH connections between AWS EC2 instances from a Windows machine.

2. Basic Linux disk and LVM (Logical Volume Management) operations including creating, formatting, mounting, and managing volumes.

# Prerequisites

1. At least one running EC2 instance (e.g., Server)

2. Access to instances via MobaXterm, Git Bash, or CMD

# Disk and LVM Management on Linux

# 1. View Block Devices
```groovy
lsblk
```

# 2. Create Mount Point for Logical Volume
```groovy
mkdir /mnt/sam_lv_mount
```

# 3. Format Logical Volume with ext4
```groovy
mkfs.ext4 /dev/test_vg/demo_lv
```

# 4. Mount Logical Volume
```groovy
mount /dev/test_vg/demo_lv /mnt/sam_lv_mount
```

# 5.Create Directory and File 
```groovy
cd /mnt/sam_lv_mount/
mkdir devops
vim demo.txt
```

# 6. View File Contents
```groovy 
cat /mnt/sam_lv_mount/devops/demo.txt
```

# 7. Unmount and Remount Logical Volume
 ```groovy 
umount /mnt/sam_lv_mount/
mount /dev/test_vg/demo_lv /mnt/sam_lv_mount
```

# 8. Mount a New Disk
  ```groovy
mkdir /mnt/sam_disk_mount
mkfs -t ext4 /dev/xvdh
mount /dev/xvdh /mnt/sam_disk_mount/
```

# 9. Check Disk Usage
 ```groovy
df -h
```

# Outcome:

1. Logical volumes and disks are formatted, mounted, and ready for use.

2. Directories and files can now be managed within the mounted volumes.
