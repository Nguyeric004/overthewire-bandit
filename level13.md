# Bandit level 13

# Objective
Find the password in data.txt which is a hexdump of a file that has been repeatedly compressed

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit12@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Found data.txt file, created temporary directory and copied contents of data.txt file to directory
    mktemp -d
    cd /tmp/tmp.ayxz3QK5pS
    cp ~/data.txt .
4. Undid hexdump on file to binary
    xxd -r data.txt data.bin
5. Checked file type
    file data.bin
6. Found file was compressed in gzip, renamed file to correct format and decompressed file
    mv data.bin data.gz
    gunzip data.gz
7. Checked contents of directory 
    ls
8. Found data file, checked file type
    file data
9. Found file was compressed in bzip2, renamed file to correct format and decompressed file
    mv data data.bz2
    bunzip2 data.bz2
10. Checked contents of directory 
    ls
11. found data file, checked file type
    file data
12. Found file was compressed in gzip, renamed file to correct format and decompressed file
    mv data data.gz
    gunzip data.gz
13. Checked contents of directory 
    ls
14. Found data file, checked file type
    file data
15. Found file was compressed in tar, renamed file to correct format and decompressed file
    mv data data.tar
    tar -xf data.tar
13. Checked contents of directory 
    ls
14. Found data5.bin file, checked file type
    file data5.bin
15. Found file was compressed in tar, renamed file to correct format and decompressed file
    mv data5.bin data.tar
    tar -xf data2.tar
16. Checked contents of directory 
    ls
17. Found data6.bin  file, checked file type
    file data6.bin
18. Found file was compressed in bzip2, renamed file to correct format and decompressed file
    mv data6.bin data.bz2
    bunzip2 data.bz2
19. Checked contents of directory 
    ls
20. Found data file, checked file type
    file data
21. Found file was compressed in tar, renamed file to correct format and decompressed file
    mv data data.tar
    tar -xf data2.tar
19. Checked contents of directory 
    ls
20. Found data8.bin file, checked file type
    file data8.bin
21. Found file was compressed in gzip, renamed file to correct format and decompressed file
    mv data8.bin data.gz
    gunzip data.gz
22. Checked contents of directory 
    ls
23. Found data file, checked file type
    file data
24. Found file was ASCII text, checked contents of file
    cat data
25. Extracted password from file
    password: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
    
# Learned
How to rename files, make temporary directories or files, decompress multiple file types and check the file's type of commpression