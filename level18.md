# Bandit level 18

# Objective
Find the password located in passwords.new and is the onlt that has changed between passwords.new and passwords.old

# Solution Steps
1. Saved RSA private key as sshkey17.private
    touch sshkey17.private
2. Log in to Bandit Server using ssh and private key file
    ssh -i sshkey17.private bandit18@bandit.labs.overthewire.org -p 2220
3. Examined contents of directory 
    ls
4. Found 2 files, passwords.new and passwords.old; compared the differences in both files
    diff -w passwords.old passwords.new
6. Double checked that difference output was indeed in passwords.new
    grep "x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO" passwords.new
    grep "CgmS55GVlEKTgx8xpW8HuWnHlBKP924b" passwords.new
5. Extracted password from output
    password: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

# Learned
How to use a local file as an ssh key and compare two files while outputting the diffreences