# Bandit level _

# Objective
Find password in data.txt file which has human-readable text and is preceded by several "="

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit9@bandit.labs.overthewire.org -p 2220
2. Examined contents of directory 
    ls
3. Found data.txt file, examined contents of file
    cat data.txt
4. Found long list of human-unreadable text, filtered for strings
    strings -a data.txt
5. Found shorter list of human-unreadable text but only strings, searched for strings that had serveral "="
    strings -a data.txt | grep "==="
6. Extracted password from file
    password: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

# Learned
How to look for only strings inside a file