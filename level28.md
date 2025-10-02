# Bandit level 28

# Objective
Clone the git repository for bandit27 and find the password.

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit27@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory 
    ls
3. Found nothing, made temporary directory for downloading of repo
    mkdir /tmp/bandit27gitclone
    cd /tmp/bandit27gitclone
4. Tried cloning repo
    git clone ssh://bandit27-git@localhost/home/bandit27-git/repo
5. Prompted error regarding using port 22 instead of port 2220, retried command with port specification
    git clone ssh://bandit27-git@localhost:2220/home/bandit27-git/repo
6. Prompted password
    upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
7. Downloaded repo, checked contents of directory
    ls
8. Found localhost:2220 directory, checked contens of directory
    cd localhost:2220
    ls
9. Found README file, checked contents of file
    cat README
10. Extracted password from file
    password: Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN
11. Removed temporary directory
    cd ..
    cd ..
    rm -rf bandit27gitclone

# Learned
How to clone a github repository using terminal and specify port when using ssh login