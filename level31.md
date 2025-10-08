# Bandit level 31

# Objective
Clone the bandit30 git repo and find the password 

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit30@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Found nothing, made temporary directory for git repo clone
    mkdir /tmp/bandit30temp
    cd mkdir /tmp/bandit30temp
4. Cloned git repo
    git clone ssh://bandit30-git@localhost/home/bandit30-git/repo
5. Checked contents of repo
    cd repo
    ls
6. Found README.md, checked contents of file
    nano README.md
7. Found no useful information, checked branches of repo
    git branch -a
8. Found no other branches, checked tags of repo
    git tag
9. Found tag labeled "secret", examined contents of tag
    git show secret
10. Extracted password from output
    password: fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

# Learned
How to check the tags of a git repo