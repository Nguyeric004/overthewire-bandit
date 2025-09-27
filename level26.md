# Bandit level 26

# Objective
Find the shell for the user bandit26 which isnt /bin/bash and break out of it after figuring out what it is

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit25@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Found sshkey for bandit26, attempted to ssh into bandit26
    ssh -i bandit26.sshkey bandit26@localhost -p 2220
4. Connection was successful but was forcefully closed immediately after authentication, checked passwd folder
    cat /etc/passwd
5. Found many shells, looked for bandit26 related content
    cat /etc/passwd | grep bandit26
6. Found location of bandit26 shell script, checked content of shell script
    cat /usr/bin/showtext
7. Found that script executes more command, looked into more command
    man more
8. Found that more displays text based on size of screen/window or one "screen full at a time" and that it can run commands through vi with command v. Checked what vi is.
    man vi
9. Found that vi is vim and that vim can run commands with the option e with prefix :. Tried more command on sshkey
    more bandit26.sshkey
10. Tried to access vim and run a random command
    v
    :e strings
11. Test was successful, tried running more in conjunction with ssh into bandit26
    :qa
    ctrl + c
    ssh more -i bandit26.sshkey bandit26@localhost -p 2220
12. Returned error, realized shell script already runs more and reduced window size of terminal to be very small to force more command to run
13. Accessed vim and checked usual place for password
    v
    :e cat /etc/bandit_pass/bandit26
14. Returned error, realized cat is not vim command, retried without cat
    :e /etc/bandit_pass/bandit26
15. Extacted password from command
    password: s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ

# Learned
How to get more information on a command, use vim, and window size vulnerabilities