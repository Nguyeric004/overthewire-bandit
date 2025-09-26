# Bandit level 24

# Objective
Look into /etx/cron.d/ for the configuration of a command being executed and find the password for bandit24

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit23@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Found nothing, moved to cron directory
    cd /etc/cron.d
4. Checked contents of directory
    ls
5. Found cronjob_bandit24 file, examined file
    cat cronjob_bandit24 
6. Found location of shell script, examined shell script
    cat /usr/bin/cronjob_bandit24.sh
7. Script executes files in /var/spool/$myname/foo ($myname is probably bandit_) then deletes them, made temp direcotry for building script
    mkdir /tmp/script23
    cd /tmp/script23
8. Created shell script using nano
    nano script23.sh
9. Made simple script that looks for bandit24 password in usual directory, then outputs the password in new file inside temp directory
    #!/bin/bash
    
    cat /etc/bandit_pass/bandit24 > /tmp/script23/password23.txt

    ctrl + x
    Y 
    ctrl + x
10. Made script executable
    chmod +x script23.sh
11. Copied script to /var/spool/bandit24/foo and waited for cronjob_bandit24.sh to execute script23.sh
    cp script23.sh /var/spool/bandit24/foo
12. No output was detected and permission was not allowed, corrected file to have all read write permissions
    chmod 777 .
    cp script23.sh /var/spool/bandit24/foo
13. Waited a little bit and then checked current directory
    ls
14. Found password23.txt file, examined contents of file
    cat password23.txt
15. Extracted password from file
    password: gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
16. Removed temp directory used for creating script
    cd ..
    rm -rf script23 

# Learned
How to make a shell script inside terminal using nano and how to give certain permissions using chmod