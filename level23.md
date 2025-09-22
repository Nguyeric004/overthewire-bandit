# Bandit level 23

# Objective
Find out what command is being executed in /etc/cron.d/, look at its shell script and determine the password

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit22@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Found nothing, moved to cron directory
    cd /etc/cron.d
4. Checked contents of directory
    ls
5. Found cronjob_bandit23 file, examined contents of file
    cat cronjob_bandit23
6. Found shell script location, examined contents of shell script
    cat /usr/bin/cronjob_bandit23.sh
7. Found pipeline inside shell script, examined variables inside shell script
    myname=$(whoami)
    mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
8. Variable myname = bandit23, used myname variable to execute mytarget pipeline
    echo I am user bandit23 | md5sum | cut -d ' ' -f 1
9. Variable mytarget = 8ca319486bfbbc3663ea0fbe81326349, used variable to examine contents of file inside /tmp/$mytarget
    cat /tmp/8ca319486bfbbc3663ea0fbe81326349
10. Extracted password from file
    password: 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

# Learned
How to read pipelines within a shell script and execute commands in an order using pipes