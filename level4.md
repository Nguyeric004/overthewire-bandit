# Bandit level 4

# Objective
Find password stored in a hidden file inside inhere directory

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit3@bandit.labs.overthewire.org -p 2220
2. Examine contents of directory
    ls
3. Found directory inhere, changed directory to inhere
    cd inhere
4. Attempted to examine contents of directory inhere
    ls 
5. Returned nothing, forced searched for all files within directory 
    ls .*
6. Found file ...Hiding-From-You, attempted to view contents of file
    cat "...Hiding-From-You"
7. Extracted password from file
    password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

# Learned
    How to search for all files within directory (including hidden files) and change directory
