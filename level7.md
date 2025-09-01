# Bandit level 7

# Objective
Find password that is owned by user bandit7, owned by group bandit6, and 33 bytes in size

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit6@bandit.labs.overthewire.org -p 2220
2. Examine contents of directory
    ls -a
3. Searched for file using size
    find . -size 33c
4. Did not find any matching file, changed directory to parent directory
    cd ..
5. Searched for file using given information
    find . -group bandit6 -user bandit7 -size 33c
6. All files found were permission denied, changed directory to parent directory
    cd ..
7. Searched again for file
    find . -group bandit6 -user bandit7 -size 33c
8. Found file path of matching file with no denial of permissions, moved directory of file
    path: ./var/lib/dpkg/info/bandit7.password
    cd ./var/lib/dpkg/info/
9. Examined contents of file 
    cat "bandit7.password"
10. Extracted password from file 
    password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

# Learned
