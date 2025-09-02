# Bandit level 11

# Objective
Find password that is encoded in base64

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit10@bandit.labs.overthewire.org -p 2220
2. Examined contents of directory
    ls
3. Found data.txt file, examined contents of file
    cat data.txt
4. Decoded text from base64
    base64 -d data.txt
5. Extracted password from file
    password dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

# Learned
How to utilize base64 command to encrypt and decrype strings
