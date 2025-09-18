# Bandit level 20

# Objective
Use setuid binary to access homedirectory of next level to gain access to password

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit19@bandit.labs.overthewire.org -p 2220
2. Check contents of directory
    ls
3. Found bandit20-do file, attempted to run file
    ./bandit20-do
4. Prompted with example use of file: ./bandit20-do id, tried other ids 
    ./bandit20-do bandit19
    ./bandit20-do bandit20
    ./bandit20-do bandit21
5. Returned permission denied, checked commands of file
    ./bandit20-do --help
6. Found information on commands, checked bandit_pass folder using setuid binary
    ./bandit20-do ls /etc/bandit_pass
7. Checked folder and file containing password using setuid binary
    ./bandit20-do cat /etc/bandit_pass/bandit20
8. Extracted password from file
    password: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

# Learned
How to use setuid binary to gain privileges of another user and access directories as that user
