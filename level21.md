# Bandit level 21

# Objective
Use setuid binary to make a connection to localhost and use the same password in previous level to get new password.

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit20@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Found suconnect file, ran file
    ./suconnect
4. Returned usage instructions, logged into Bandit Server on another instance
    ssh bandit20@bandit.labs.overthewire.org -p 2220
5. Use netcat to create listening server with arbitrary port
    netcat -l -v -p 2000
6. Ran suconnect file on other instance to connect to netcat server
    ./suconnect 2000
7. Prompted previous password
    0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
8. Extracted password from output
    password: EeoULMCra2q0dSkYj561DX7s1CpBuOBt


# Learned
How to create a listening server with netcat and specify commands with netcat