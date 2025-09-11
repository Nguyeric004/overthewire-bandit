# Bandit level 15

# Objective
Find password by submitting previous found password into port 30000 on localhost

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit14@bandit.labs.overthewire.org -p 2220
2. Examined contents of directory
    ls
3. Found nothing, attempted to connected to port 30000 as user bandit14
    ssh -i MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS bandit14@localhost -p 30000
4. Returned error, no such file, retried connection of port 30000 using telnet instead
    telnet 127.0.0.1 30000
5. Entered in current password, returned password for next level
    password: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

# Learned
How to connect to a port using telnet