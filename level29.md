# Bandit level 29

# Objective
Find the password for bandit29 in the git repository for bandit28

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit28@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Found nothing, made temporary directory for git repo cloning
    mkdir /tmp/bandit28temp
    cd /tmp/bandit28temp
4. Cloned git repo on port 2220
    git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
5. Checked contents of directory
    ls -a
6. Found .git and README.md file, checked README.md file
    cat README.md
7. Found some notes for bandit29 but no password, checked .git directory
    cd .git
    ls
8. Found logs directory, checked contents of directory
    cd logs
    ls
9. Found HEAD file, checked contents of file
    cat HEAD
10. Found information regarding commit of a change in repo inside HEAD file, checked all git changes
    git log
11. Found history of commits in git repo, checked commit described with "fix info leak"
    git show 710c14a2e43cfd97041924403e00efb00b3a956e
12. Extracted password from display of changes to README.md file
    password: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7
    
# Learned
How to check the commit logs of a github repo
