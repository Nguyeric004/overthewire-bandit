# Bandit level 19

# Objective
Find the password stored in a 'readme' file in homedirectory.

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit18@bandit.labs.overthewire.org -p 2220
2. Immediately forced to log out
3. Tried reading file without interacting with shell
    ssh bandit18@bandit.labs.overthewire.org -p 2220 cat 'readme'
4. Extracted password from output
    password: cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

# Learned
How to use non-interactive ssh commands