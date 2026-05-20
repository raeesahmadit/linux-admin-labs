Linux stores data in hierarchy of directories and files.
in Linux path define with forward slash ' / '      but in windows ' \ '
Linux is case sensitive 
no problem with extensions in Linux

---------------------------------------------------------------------------------------------------------------
Types of File system:
 - ext3
 - ext4   mostly in Ubuntu
 - XFS    mostly in centOs
 - BtrFS (B-tree FS) (Open SUSE and Suse Linux Enterprise Server)
 - FAT

Check file system in your Linux : lsblk -f,     dh -Th,     cat /etc/fstab

XFS : Optimized for large files, offering superior performance and scalability and parallel processing
ext4: Perfrom will across various file sizes but less efficient with extremly large files

----------------------------------------------------------------------------------------------------------------
Inode : a data structure in Linux which stores matadata of a file or directory, file system use inode number to
        to locate the inode, which then contains the pointer to the data-blocks where the actual file is stored
       
----------------------------------------------------------------------------------------------------------------
/ (root directory, parent directory) : from this all other files and directories branch out (like c:\ drive in windows)

/bin : have all executable commands binary details, like: ls, pwd, cd, whoami, etc.. (like program file, windows in window)

/sbin : same as bin, but have mostly system admin needed files, system managment command files like: fdisk, shutdown, ip etc.. 

/etc : have all configration files, like: User, Network, Services, etc   (like programfiles, system32 in windows)

/home : is personal directories of all users (like c:\users in windows, need permission)

/root : is home directory of root/super user a sperate directory of root

/var : have all variable data such as logs and database (imp for troubleshooting)
       boot.log , secure, messages(system general logs) etc..
/boot : have all to system boot-up, include the Linux kernel, initial RAM disk image, Bootloader configrations (like GRUB)

/dev : (device folder) have hardware devices files likes hard-drive, keyboard, mouse etc

/lib, lib64 : have all shared libraries and kernel modules use to boot and run commands in the root filesystem
              lib64 have same thing but support 64-bit apps

/media : have all files related to external devices like USB etc..

/mnt : similar to media, traditional mount point, where system admin mount temporary filesystem while configuring them

/opt : third-party packages module place here to avoid cluttering the system directories

/proc : it is virtual and dynamic directory it only exist in memory does not use disk, have all the info about 
        system resources, hardware, and running processes

/sys : similar to /proc, another virtual filesystem that provides interface to kernel, have info and setting about
       system devices, drivers and kernel features

/run : have temporary filesystem which stores state file like: process IDs, lock files, it cleared and recreated after every boot

/srv : have all data which serves to hosts on the system like: web pages served by web server, ftp for file shared

/tmp : store system processes and user applications temporary data, modern systems mount this directory in volatile memory (tmpfs)
       all data clear when reboot or shutdown

/usr : (second-level-hierarchy) : have all user apps and varitey of other things for day-to-day operations,
       include libraries, documentation, etc.., subdirectories like /usr/bin, /usr/sbin, /usr/local, /usr/share, /usr/include etc..
      everything provided at this place for users as it is 2nd-level-hierarchy what every changes we done so not our main
      system could impact

 