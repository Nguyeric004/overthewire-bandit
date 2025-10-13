# Bandit level 33

# Objective


# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit32@bandit.labs.overthewire.org -p 2220
2. Prompted "WELCOME TO THE UPPERCASE SHELL", tried checking contents of directory
    ls
3. Returned error, permission denied with command being written in uppercase. Tried command in uppercase
    LS
4. Returned same error, tried commands that did not rely on lettering
    $0
5. Broke out of >> user and became $ user, tried checking directory path
    pwd
6. Returned directory path, tried looking for password file
    cat /etc/bandit_pass/bandit33
7. Extracted password from output
    password: tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0

# Learned
How to take exploit positional paramter vulnerabilities