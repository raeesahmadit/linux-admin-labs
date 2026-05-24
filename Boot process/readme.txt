BIOS 
   > MBR
        > GRUB
             > Kernel
                    > SystemD

BIOS: 
    -First program that executed which is stored in read-only memory on motherboard
    -Perform POST (power-on self-test) verify the hardware components
    -Check the bootable device like pendrive, hardisk
    -Handover control to first sector of device : MBR
    other than this UEFI (Unified Extensible Firware Interface) i sused.

MBR(Mater Boot Record): 
   -512 bytes, first sector of any bootable device contain machine code instructionts
     to boot a machine
             Boot loader (446 bytes)
             Partition Table (64 bytes)
             Error Checking (2 bytes)
    -it will load the boot loader into the memory and handover to it

GRUB(Grand Unified Boot loader):
    -load /boot/grub2/grub.cfg at boot time
    -at this stage user see the GUI asking different OS or Kernel
    -once you selected the Kernel, it locates the coresponding Kernel binaray
        /boot/vmlinuz-<kernel-version>
    -main job is to load a kernel and initrd/initramfs image into memory
    -once load kernel in to ram, it passes control to it
    in RHEL7 Default boot loader is grub2
    GRUB is for x86 architecture, it could be different for others architecture
       like for intel Itanium- ELILO

Kernel: 
   -loaded into read-only mode 
   -initramfs/initrd gets decompressed and load 1st temporary file system
   -initrd then detects and load drivers from temporary filesystem to actual filesystem
   -mount other partitions like LVM, RAID etc. and unmount itself
   -once main filesystem is mounted, kernel inirialize the 1st process init/SystemD
    you can see these images under /boot folder

SystemD:
   -1st service loaded with process ID 1
   -start all required processes
       /etc/systemd/system/default.target
   -to bring the system to the run-level/target (0-6)
       to see current default target : systemctlget-default
   - you can find different runlevels files under
      /usr/lib/systemd/system ---> ls -l runlevel*