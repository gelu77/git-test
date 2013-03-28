# Git Commands

Init git repository

    git init
    git add README
    git commit -m "first commit"
    git remote add origin git://github.com/gelu77/MyRepo1.git
    
Clone from an existing git repository

    git clone git://github.com/gelu77/MyRepo1.git
    
Commit the changes of tracked files

    git commit -am "change for tracked files"
    
Push the local changes to remote repository

    git push -u origin master
    
Pull the remote changes into the local repository

    git fetch origin
    git merge origin/master
Or the simple command

    git pull origin
[How do you discard unstaged changes in git?](http://stackoverflow.com/questions/52704/how-do-you-discard-unstaged-changes-in-git)

1.

    git stash save --keep-index
    git stash drop
2.

    git checkout path/to/file/to/revert
    git checkout -- .
    
3.

    git clean -df & git checkout -- .

[git: undo all working dir changes including new files](http://stackoverflow.com/questions/1090309/git-undo-all-working-dir-changes-including-new-files?answertab=active#tab-top)

1.

    git reset --hard # removes staged and working directory changes
    git clean -f -d # remove untracked files
    
[Removing multiple files from a Git repo that have already been deleted from disk](http://stackoverflow.com/questions/1402776/how-do-i-commit-all-deleted-files-in-git)

1.

    git add -u

2. 

    git ls-files --deleted | xargs git rm
    git commit



