# p3main

 gedit file1.txt
git init
 git checkout -b"sourcebranch"
 gedit file1.txt
 git add file1.txt
 git stash save "file1 modified"
 
 git checkout master
 gedit file1.txt
 git add file1.txt
git commit -m "file1 cheched and changed"

 git checkout -b"targetbranch"
 gedit file1.txt
 git stash apply
 git add file1.txt
 git commit -m "file1 updated successfully"
gedit file1.txt
 git checkout master
 gedit file1.txt
 git merge "targetbranch"
 gedit file1.txt
git branch --list
 git stash list
 git stash drop stash@{0}
