# Bandit level 3

# Objective
    Find password in file --spaces in this filename-- 

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit2@bandit.labs.overthewire.org -p 2220
2. Examine contents of directory
    ls
3. Found file --spaces in this filename-- and attempted to look at contents usiong file path
    cat ./--spaces in this filename--
4. Search returned error, attempted to clarify specification of file using quotations
    cat ./"--spaces in this filename--"
5. Extracted password from file
    password: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

# Learned
    How to specify exact filename using quotations instead of just filepath
