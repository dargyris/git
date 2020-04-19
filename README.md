# Git list of commands

## Introduction
0. git version
1. git config --global user.name "my_name"
                       user.email "my_email"
                       core.editor "vim"
                       diff.tool p4merge
                       difftool.p4merge.path
                       difftool.prompt false
                       merge.tool p4merge
                       mergetool.p4merge.path
                       mergetool.prompt false
                       --list   lists config
                       -e       opens conf in vim
                       alias.<command_name> "command"
       eg.:            alias.hist "log --all --graph"
   vim ~/.gitconfig
2. git ll               show history
3. git log              show commit history
4. git ls-files         lists tracked files
5. git help <command>

.gitignore              vim .gitignore

# Adding stuff
1. git init
2. git clone    [get address from github]
3. git status   
4. git add      <file>
                .       recursive add for trees
                -A      add and update all changes
                        helps with mv and rm
                -u      update
5. git commit           invokes editor for msg.
                -m      inline message
                -am     for existing file
6. git push     origin master
7. git pull     origin master

# Deletion
1. git rm               <file>
          --cached      <file> stops tracking
2. git mv               <file> <target>
3. git reset HEAD       <file> Back out change
4. git checkout --      <file> Restore file
5. git restore --staged <file> 

# History
1. git log                   git commit history in 
                             reverse chronolog. order.
            --abbrev-commit
            --oneline --graph --decorate
            --all --graph --decorate --oneline
            d2a3cc1...219a253
            --since="2 days ago"
            -- <file>
            --follow -- <file_path>
   git show <long commit id from git log command>

# Diff and Merge
1. git diff               Working dir vs Staging area
            HEAD          Working dir vs last commit
            --staged HEAD Staged area vs last commit
            -- <file>     Only for the file I want
            bc8a183 HEAD  Get from git log --oneline
            HEAD HEAD^    HEAD with HEAD-1
            bc8a183 ad1243a
            master origin/master
2. git difftool           Invokes p4merge
            All commands from diff apply the same
