1. find a file with name : find . -iname file1
   '.' mean current location
   -iname will find for name and ignore case sensitivity

2. find a file with size : find . -size +50M -size -100M
   -size will find on the base of size of the file 
   +50M -100M mean file larger then 50M and smaller then 100M
   byte = c    ,    mb = M
   
3. find with respect to file type : find . -type f
   -type = f-file   d-directory   l-symbolic link   
           b-block device    s-socket

4. find a file for a user : find . -user root

5. find a file form a inode : find . -inum 33652705
   to see a inode number ls -li  it will give a inode number of file

6. find a file from num of links : find . -links 3
   to see links  ls -ltr  you can see links

7. find a file on the base of permission: find . -perm /u=r
                                 : find . -perm /777
    to know permission go to permission folder

8. find a file created after mentioned file : find . -newer lastfile.txt 

9. find a all the empty files (imp): find . -empty

10. find empty file and delete at same time (v-imp) :
                                   find . -empty -exec rm {} \;
    -exec rm {} \;   it will remove file and you can use other veriants too..
    -exec rmdir \;   it will remove empty direcctory

11. find files 15 days old : find . -mtime 15 