other than chmod and chown chgrp there is another smart way
ACL (Access Control List) Permission
it allows to give more specific permissions to a file or a 
directory without changing the base ownership and permissions
mean for sometime we give access to another user but the main 
owner remain the same

1. to see the permissions:    getfacl file1

2. to add a file permission for a user: setfacl -m u:ibtu:rwx file1
           -m = modification
            u = user

3. to add a file permission for group: setfacl -m g:root:rw file2
            g = group

4. to remove a entry: setfacl -x u:user:rwx file3

5. to move all old entries: setfacl -b file4

6. to add permission for a directory: setfacl -Rm rwx files/

7. if the acl is set then there will be a '+' sign will added at permission area


