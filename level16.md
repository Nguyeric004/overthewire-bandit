# Bandit level 16

# Objective
Find the password for next level by submitting current password to port 30001 on localhost using SSL/TLS encryption.

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit15@bandit.labs.overthewire.org -p 2220
2. Examined contents of directory
    ls
3. Connected to port 30001 on localhost using SSL/TLS
    openssl s_client -connect localhost:30001
4. Returned details of certificates and ssl session, enterend in current password and extracted next level password
    password: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

# Learned
How to connect to a port using SSL/TLS encryption