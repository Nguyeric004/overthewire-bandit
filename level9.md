# Bandit level 9

# Objective
Find password in data.txt file that occurs only once

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit8@bandit.labs.overthewire.org -p 2220
2. Examine contents of directory
    ls
3. Found file data.txt, filtered out repeating lines of text
    uniq -u data.txt
4. Command returned long list of texts, sorted list before filtering
    sort data.txt | uniq -u
5. Extracted password from file
    password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

# Learned
How to filter lists using uniq and its prefixes, sorting lists with sort, and chaining commands together with |