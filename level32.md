# Bandit level 32

# Objective
Clone the bandit31 git repo and find the password 

# Solution Steps
1. Log in to Bandit Server using ssh
    ssh bandit31@bandit.labs.overthewire.org -p 2220
2. Checked contents of directory
    ls
3. Created temp directory for cloning git repo
    mkdir /tmp/bandit32temp
    cd /tmp/bandit32temp
4. Cloned repo on port 2220
    git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo
5. Checked contents of directory
    ls
6. Found repo directory, checked contents of directory
    cd repo
    ls
7. Found README.md file, checked contents of file
    cat README.md
8. Found isntructions to push key.txt file with message "May I come in?" to remote repository. Created key.txt file
    echo "May I come in?" >> key.txt
9. Tried to add key.txt file to repo
    git add key.txt
10. Returned error stating file is ignored, checked .gitignore 
    cat .gitignore
11. Found *.txt in .gitignore file, checked file
    cat *.txt
12. File contained "May I come in?", deleted file
    rm *.txt
13. Tried adding key.txt file to repo
    git add key.txt
14. Add was successful, commited changes to repo
    git commit -m "key.txt added"
15. Commit was successful, pushed chages to repo
    git push origin master
16. Extracted password from output
    password: 3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K
17. Removed temp directory
    cd ..
    rm -rf bandit32temp

# Learned
How to update a git branch and repo while also adding ignore options for certain files