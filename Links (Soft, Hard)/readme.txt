1. to make a soft link of a file: ln -s ./folder/file1.txt file1-shotcut
    -s mean softlink
    it is like shotcut in windows we can make shortcut of a main file anywhere
    but in soft link if you delete main file link file will broke.
    file will represented as 'l' at starting, if the file turn in to 
    red color mean the link is broken

2. to make a hard link of a file: ln ./folder/file2.txt file2.shortcut
   same like soft link but the shortcut file will not be damaged if
   main file deleted, represented as a normal file