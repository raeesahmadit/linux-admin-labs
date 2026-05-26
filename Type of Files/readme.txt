
1. s - socket files : to enable communication between two processes, .sock
                     these are in /run folder
    to find these : find / -type s

2. p - FIFO or Named-pipe: send data from one process to another so that the reciving process reads
                           the data first-in-first-out manner
    to make FIFO files: mkfifo filename
    to find these : find / -type p

3. b - block device file : these refer to a device
    to find these : find / -type b

4. c - character device file : these reads/writes data in characterby character
                     these are in /dev folder
    to make character file : mknod
    to find these : find / -type c
5. l - link 

6. - regular files

7. d - directory

