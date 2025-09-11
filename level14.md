# Bandit level 14

# Objective
Find the password located in /etc/bandit_pass/bandit14 which can only be read by user bandit14 using the provided private SSH key.

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit13@bandit.labs.overthewire.org -p 2220
2. Examine contents of directory
    ls
3. Found sshkey.private file, examined file
    cat sshkey.private
4. Attempted to ssh into next level as bandit 14 using sshkey.private
    ssh -i sshkey.private bandit14@localhost
5. Returned error; invalid connection through port 22, retried ssh while specifying correct port
    ssh -i sshkey.private bandit14@localhost -p 2220
6. SSH was successful, located file containing password
    cd /etc/bandit_pass
7. Found bandit14 file, extracted password from file
    cat bandit14
    password: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

# Learned
How to SSH locally and using a private ssh key.