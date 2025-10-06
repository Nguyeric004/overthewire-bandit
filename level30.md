# Bandit level 30

# Objective
Download the bandit29 git repo and find the password 

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit29@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Found nothing, made temporary directory for git repo cloning
    mkdir /tmp/bandit29temp
    cd /tmp/bandit29temp
4. Cloned repo on port 2220
    git clone ssh://bandit29-git@localhost/home/bandit29-git/repo
5. Checked contents of repo directory
    cd repo
    ls -l
6. Found README.md file, checked contents of file
    nano README.md
7. Did not find password, checked git logs
    git log
8. Found previous commit with "fix username" description, checked commit
    git show 873b7f66c519fabdfcbdde431d75921d2cea369d
9. Did not find password, checkted contents of repo directory
    ls -la
10. Found branches directory, checked contents of directory
    cd branches
    ls -la
11. Found nothing, checked git branches
    git branch
12. Found master branch, switched to master branch
    git checkout master
13. Checked contents of directory
    ls
14. Found README.md file, checked contents of file
    nano README.md
15. Did not find password, checkd all git branches
    git branch -a
16. Found list of remote branches, checked branches starting from the top
    git checkout dev
    ls -la
17. Found README.md file, checked contents of file
    nano README.md
18. Extracted password from file
    password: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

# Learned
How to check and switch branches using git commands