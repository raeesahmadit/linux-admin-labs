grep is use to find a pattern or word
1. ignore case-sensitive : grep -i  umaima file2.txt
   umiama and UMAIMA and Umaima and umaIma all are different words
   -i use to ignore these
   grep find umaima in file2.txt

2. search everything other then given word : grep -v umaima file2.txt
   -v will left given word and show everything else

3. count a word in a data : grep -c qundeel file2.txt
   -c count given word in a file2.txt

4. fetch exact word : grep -w umaima file1.txt
   -w exact word to search

5. see on which line the data is: grep -n raees file1.txt

6. find data in multiple files: grep -i raees file1.txt file2.txt
   even in different format files

7. find multiple data in a file: grep -e umaima -e qundeel -e raees file1.txt
                               : egrep "umaima|qundeel|raees" file1.txt

8. find a names in files from another file: grep -f file1.txt file2.txt file3.txt
   -f it will find the words in following files which are in given file
   only show data with names will avaliable in file1 and also in file2, file3

9. show data which start from given word: grep ^r file1.txt
   ^ it is header sign mean start with

10. show data which end with given word: grep ees$ file1.txt

11. find a word inside given directory: grep -R "raees" foldername/
    it will find word in all the files in the folder

12. to see previous command was successful or not: echo$?
    0 mean successful
    1 mean unsuccessful
    