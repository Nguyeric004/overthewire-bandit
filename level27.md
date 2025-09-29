# Bandit level 27

# Objective
Find the password for bandit27

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit26@bandit.labs.overthewire.org -p 2220
2. Authentication was successful but connection was closed immediately, tried window size exploit
    v
    :e /etc/bandit_pass/bandit27
3. Permission to file was denied, checked shell of vi
    :set shell
4. Found shell is /usr/bin/showtext, changed shell to /bin/bash
    :set shell = /bin/bash
5. Checked shell
    :set shell
6. Confirmed shell has been changed, ran shell
    :shell
7. Able to run commands as bandit26, checked contents of directory
    ls
8. Found bandit27-do file, checked file
    nano bandit27-do
9. File contains human-unreadable text and is unwritable, checked type of file
    file bandit27-do
10. Found file is a setuid executable, ran file
    ./bandit27-do
11. Prompted example on how to use file, ran file to search for password as bandit27
    ./bandit27-do cat /etc/bandit_pass/bandit27
12. Extracted password from output
    password: upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB

# Learned
How to change shell inside of vi
