we use pip sigh " | " to assign output of first command as an input of second command.

1. -to count the folders/files in a direcctory:   ls -1 | wc -l
    ls -1 show all folders/files in seperate lines and then its output will send to 
    wc -l to count the lines

2. -to output combine data of two files:          cat file1.txt file2.txt | sort
    cat file1.txt file2.txt  it will combine the data and
    sort will sort the data and output

3. -to output unique data in two files:           cat file1.txt file2.txt | sort | uniq
    to get unique we first to sort and we did it earlier and 
    uniq will output only single time

4. -see selective lines from a file :          cat file1 file2 | head -3 | tail -1
    head will select only first 3 lines and 
    tail will show only last 1 lines of those 3 lines

5. -to see or save the output in a file :         ls | tee file.txt | wc -l
    ls show the files/folders 
    tee with save in file.txt and also display on screen
    wc -l will count the lines how much data saved in file.txt

6. -to pass a 1st command as a text to second command:   ls | xargs echo 
    ls all data will bass as a command to echo 
    echo will show every thing as it is

   - to make files with single command :      cat file.txt | xargs touch
    cat file.txt will show all the data in file.txt and
    touch with make all files with those names but
    xrags will give output names as a test to touch