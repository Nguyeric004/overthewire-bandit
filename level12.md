# Bandit level 12

# Objective
Password has been rotated by 13 positions

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit11@bandit.labs.overthewire.org -p 2220
2. Examined contents of directory
    ls
3. Found data.txt file, examined contents of file
    cat data.txt
4. Found encoded text, put text through rot13 decoding algorithm
    strings -a data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
5. Extracted password from file
    password: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

# Learned
How to use tr command to map and translate inputs and outputs