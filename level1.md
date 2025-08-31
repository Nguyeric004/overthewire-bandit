# Bandit level 1

# Objective
Find password stored in readme file.

# Solution Steps
1. Login to Bandit Server using ssh.
    ssh bandit0@bandit.labs.overthewire.org -p 2220
2. looked at home directory contents
    ls
3. Found file "readme" and looked at contents
    cat "readme"
4. Extracted password from contents
    password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

# Learned
How to navigate a directory and look at contents inside a specified file.