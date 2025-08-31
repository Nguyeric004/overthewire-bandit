# Bandit level 5

# Objective
Find password in human-readable file inside inhere directory

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit4@bandit.labs.overthewire.org -p 2220
2. Examine contents of directory
    ls
3. Found directory inhere, changed directory to inhere
    cd inhere
4. Attempted to examine contents of directory inhere
    ls
5. Found files -file00, -file01, -file02, -file03, -file04, -file05, -file06, -file07, -file08, -file09, attempted to examine contents of all files
    cat ./*
6. Returned human-unreadable data, attempted to examine contents of each file instead of all at once
    cat ./-file00 ... cat./-file09
7. Extracted password from file -file07
    password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

# Learned
    How to concatenate all files within directory as well determine difference between human-readable and human-unreadable data