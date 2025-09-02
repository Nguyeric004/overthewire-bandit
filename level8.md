# Bandit level 8

# Objective
Find the password stored in file data.txt next to word "millionth"

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit7@bandit.labs.overthewire.org -p 2220
2. Examined contents of directory
    ls
3. Found data.txt file, examined contents of file
    cat data.txt
4. File contained numerous lines of text, searched for specific word within file
    grep "millionth" data.txt
5. Extracted password from search
    password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

# Learned
How to use grep command to find specific text within a file