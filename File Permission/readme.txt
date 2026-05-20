
0 123 456 789   10     11 
| ||| ||| |||   |      |
d rwx r-- r--  ibtu   ibtu
- rw- --- ---  ibtu   ibtu
d rwx rwx rwx  ibtu   ibtu
  
 at place 0                r = read
 - = file                  w = write
 d = directory             x = executable
                           - = nothing other then 0 place 

0   = type of file
123 = user permissions
456 = group permissions
789 = other permissions
10  = owner of file
11  = group 
-------------------------------------------------------------------------------------------------------

      u = user
      g = group
      o = other
      a = all 

Modify permission of a file :
    way1:       chmod a+rwx file1 -this will give all rwx to file
                chmod g-wx file1  -this will remove the w and x permission to a group
                chmod u-w file1   -this will remove the w permission to a user
                chmod o-rwx file1 -this will block all permissions to others
    
    way2:       chmod u=rx file2  -this will give r and x to user
                chmod g=w file2   -this will give w to group
    
    way3(octal/numeric method):
                chmod 777 file3  -this will give all permissions to every owner
                chmod 000 file3  -this will remove all permissions
                chmod 740 file3  -this will rwx to user and r to group and no permission to others
        
        chmod (u)(g)(o) file3

        0: No permission       
        1: x                   
        2: w                   
        3: xw (2+1)
        4: r
        5: rx(4+1)
        6: rw(4+2)
        7: rwx(4+2+1)

Modify permission of a Directory and all files in it:
                chmod -R u=r files/  -this will give user only r permission to a folder
                chmod -R o=wr files? -this will give other w and r permission to a folder
----------------------------------------------------------------------------------------------------

Change Ownership of files:        chown (user):(group) file4
                                  chown ibtu:ibtu file4
Change Ownership of Directory: chown -R ibtu:root file4
-----------------------------------------------------------------------------------------------------

Only change group:    chgrp (group) file5
                       chgrp root file5



