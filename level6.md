# Bandit level 6

# Objective
Find password given that the file is human-readable and has a size of 1033 bytes

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit5@bandit.labs.overthewire.org -p 2220
2. Examine contents of directory
    ls
3. Found inhere directory, changed directory to inhere
    cd inhere
4. Examine contents of inhere directory
    ls
5. Found multiple directories of maybehere followed by numbers, checked disk usage of all files in human-readable format
    du -h .
6. Did not find file size that matched 1033 bytes, searched all files for specific file size instead
    find . -size 1033c
7. Found .file2 in maybehere07 directory to match size, changed directory to maybehere07 and examined all contents of directory
    cd maybeher07
    ls -a
8. Found .file2, examined contents of file
    cat ".file2"
9. Extracted password from file
    password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

# Learned
How to search for files based on size