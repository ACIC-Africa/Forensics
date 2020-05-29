# Forensics Summarized

- [Disk Analysis](#disk-analysis)
- [Types of Disks](#types-of-disks)

---

## Disk Analysis
### Types of Disks
- [Magnetic Storage Drives](https://en.wikipedia.org/wiki/Magnetic_storage) - Use Magnets to read and write (Example: Magnet Tapes)
- [Optical Storage Drives](https://en.wikipedia.org/wiki/Optical_storage) - Use laser beams to read binary data (Example: CD, DVD)
- [Flash Memory Devices](https://en.wikipedia.org/wiki/Flash_memory) - Non-volatile memory that can retain data in memory. (SSD Drives, BIOS Chip, Memory Cards)
- [Hard Disk Drive (HDD)](https://en.wikipedia.org/wiki/Hard_disk_drive) - Non-volatile memory that stores data magnetically.
- [Solid State Drive (SSD)](http://en.wikipedia.org/wiki/Solid-state_drive) - Non-volatile memory that implements Solid state technology to store dat like a hard disk drive. Uses NAND Based SSD to store data even after power failure and Volatile RAM-based SSD for fast data access.
### Logical System Structure
The logical system structure ccontrols how data is arranged and read on the system.
- [FAT](https://en.wikipedia.org/wiki/File_Allocation_Table) - Originally designed for floppy disks and used on DOS and Windows 9x systems.
- [FAT32](https://en.wikipedia.org/wiki/File_Allocation_Table#FAT32)
- [NTFS](https://en.wikipedia.org/wiki/NTFS) - Supported on Windows, Linux, BSD and read-only support on macOS
- [EXT](https://en.wikipedia.org/wiki/Extended_file_system) - UNIX
- [EXT 2](https://en.wikipedia.org/wiki/Ext2) - exist in GNU Hurd, MINIX 3, some BSD kernels, in MiNT, and as third-party Microsoft Windows and macOS drivers.
- [EXT 3](https://en.wikipedia.org/wiki/Ext3)
- [EXT 4](https://en.wikipedia.org/wiki/Ext4)
- [EFS](https://en.wikipedia.org/wiki/Extent_File_System)
### Hard Disk Interfaces
This are cables or devices used to interface between the hard drive and the computer.
- [Serial ATA (SATA)](https://en.wikipedia.org/wiki/Serial_ATA) - Channel between motherboard and hard drive
- [Small Computer System Interface (SCSI)](https://en.wikipedia.org/wiki/SCSI) - Interface between computer and CD drives,printers, scanners or disk drives.
- [Serial Attached SCSI](https://en.wikipedia.org/wiki/Serial_Attached_SCSI) - Handles data flow between storage devices.
- [ATA/PATA (IDE/EIDE)](https://en.wikipedia.org/wiki/Parallel_ATA)
### Hard Disk Sectors
This are cables or devices used to interface between the hard drive and the computer.
- Clusters: Are smallest accessible storage units on a hard disk
- Slack: The area of the file and the end of the cluster. Slack space ma contain deleted data.
  - RAM Slack
  - Drive Slack
- Lost / Orphan Cluster: Operating systems mark clusters as used even though they do not contain any files. This may occur due to disk corruption or not closing a file or when a user shuts down a comuter without closing applications.
- Bad Sectors: Damaged portion of the disk that do not support read and write operations.

### Hard Disk Partitions
Creation of logical drives for effective memory management
- Primary partition: Holds operating system and system area information required for booting
  - Boot Sector: 
    - BIOS Parameter Block: Contains information about the physical layout of the disk and file system layout. This is used to locate the file table on the hard drive.
    - [Master boot Record (MBR)](https://en.wikipedia.org/wiki/Master_boot_record): Holds the partition table and stores information on the files on the disk. It also contains executable code to load the installed operating.
    - Master Boot Code: Finds the active partition used in boot loading process in order to load the operating system (OS)
- Extended partition: Holds information on data and files stored


### Hard Disk Forensics Tools
- [Autopsy](https://www.sleuthkit.org/): A digital forensics platform and GUI for The Sleuth Kit (TLK) used for:
  - Timeline analysis
  - PhotoRec: Recover deleted files from unallocated space
  - Hash filtering
  - Keyword searches
  - Extract web activity
  - View images
  - Search for indicators of compromise using Stix.
- Chkdsk.exe: Default Windows utility (C:\Windows\System32\chkdsk.exe) that detects and repairs bad sectors or errors in file systems and disks.
- [The Sleuth Kit (TLK)](https://www.sleuthkit.org/): A set of tools used to analyze disk images and review the disk layout, history, partitions and file system.
  - fstat: General details of the file system
  - istat: Details of metadata structure
  - fls: List files and directory files in a disk image
  - img_stat: Display details of an image file
- [Active@ Disk Editor](https://www.disk-editor.org/index.html): Used to examine disk partitions
- [HxD - Freeware Hex Editor and Disk Editor](https://mh-nexus.de/en/hxd/): Used for raw disk editing and modifying of main memory (RAM).
- [WinHex Hex Editor](http://www.winhex.com/winhex/hex-editor.html): Used for raw disk editing and modifying of main memory (RAM).
- [Hex Workshop](http://www.hexworkshop.com/): Used for raw disk editing and modifying of main memory (RAM).
- dd: Backup MBR on a Linux system.

## Mobile Forensics
Recovering forensic data from a mobile device. This includes extraction of data from the SIM card, Internal memory card and SD card.
### Mobile Architecture
- Client Application
- Communication API, Phone API, GUI API and Middleware Components
- Operating System
- Hardware
- Radio Interface, gateway and network interface
- Network
