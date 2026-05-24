1. to see all running processes : ps -e |more
        more detailed           : ps -ef | more 
        more and more detailed  : ps aux 

2. to see detials of a specific process : ps -ef | grep 'specific-name'

3. to see process of specific user : ps -u ibtu
   to see process of a specific group : ps -G ibtu

4. to see process into processes tree view : ps -ejh