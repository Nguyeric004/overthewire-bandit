# Bandit level 22

# Objective
Look at cron configuration inside /etc/cron.d/ for what command is being executd and password

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit21@bandit.labs.overthewire.org -p 2220
2. Check contents of directory
    ls
3. Found nothing, moved to cron.d directory
    cd /etc/cron.d
4. Check contents of directory
    ls
5. Found cronjob_bandit22 file, checked file
    cat cronjob_bandit22
6. found shell script, checked shell script
    cat /usr/bin/cronjob_bandit22.sh
7. Found location of password, checked file location 
    cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
8. Extracted password from file
    password: tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

# Learned
How to read cron files and change mode command permissions for a file