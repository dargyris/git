===================================================
Introduction
---------------------------------------------------
0. git version
1. git config --global user.name "my_name"
              --global user.email "my_email"
              --global core.editor "vim"
              --global --list
2. vim ~/.gitconfig
1. git 
2. git ll               show history
3. git log              show commit history
4. git ls-files         lists tracked files
5. git help <command>

===================================================
Adding stuff
---------------------------------------------------
1. git init
2. git clone    [get address from github]
3. git status   
4. git add      <file_name>
                .       recursive add for trees
                -A      add and update all changes
                        helps with mv and rm
                -u      update
5. git commit           invokes editor for msg.
                -m      inline message
                -am     for existing file
6. git push     origin master
7. git pull     origin master

===================================================
Deletion
---------------------------------------------------
1. git rm               <file_name>
2. git mv               <file_name> <target>
2. git reset HEAD       <file_name> Back out change
3. git checkout --      <file_name> Restore file
4. git restore --staged <file_name> 

===================================================
History
---------------------------------------------------
1. git log              git commit history in 
                        reverse chronolog. order.
            --abbrev-commit
            --oneline --graph --decorate
            d2a3cc1...219a253
            --since="2 days ago"
            -- <file_name>
            --follow -- <file_path>
   git show <long commit id from git log command>
