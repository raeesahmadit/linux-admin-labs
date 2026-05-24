1. to check system memory avaliable     : df -h
                    to see in kilobites : df -h -BK
                    to see in Gigabites : df -h -BG

2. disk utilization = du                 : du -h
    to see how much a folder use storage : du -h /home/ibtu/files/
    to see all files in a folder storage : du -ah /home/ibtu/files/
    to see total volume used by a folder : du -ahc /home/ibtu/files/

3. to check free memory                  : free -h 
   show you continus update evry 2 sec   : free -h -s 2
   show after every given sec  (4 time)  : free -h -c 4 