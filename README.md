# p3main

git@ise:~$ mkdir 1mv23ai002
git@ise:~$ cd 1mv23ai002
git@ise:~/1mv23ai002$ mkdir exp3
git@ise:~/1mv23ai002$ cd exp3
git@ise:~/1mv23ai002/exp3$ gedit file1.txt
git@ise:~/1mv23ai002/exp3$ git init
Initialized empty Git repository in /home/git/1mv23ai002/exp3/.git/
git@ise:~/1mv23ai002/exp3$ git add file1.txt
git@ise:~/1mv23ai002/exp3$ git commit -m"file1 created"
[master (root-commit) c98960d] file1 created
 1 file changed, 1 insertion(+)
 create mode 100644 file1.txt
git@ise:~/1mv23ai002/exp3$ git checkout -b"sourcebranch"
Switched to a new branch 'sourcebranch'
git@ise:~/1mv23ai002/exp3$ gedit file1.txt
git@ise:~/1mv23ai002/exp3$ git add file1.txt

git@ise:~/1mv23ai002/exp3$ git stash save "file1 modified"
Saved working directory and index state On sourcebranch: file1 modified
git@ise:~/1mv23ai002/exp3$ git checkout master
Switched to branch 'master'
git@ise:~/1mv23ai002/exp3$ gedit file1.txt

git@ise:~/1mv23ai002/exp3$ git add file1.txt
git@ise:~/1mv23ai002/exp3$ git commit -m "file1 cheched and changed"
[master 92f9523] file1 cheched and changed
 1 file changed, 1 insertion(+)
git@ise:~/1mv23ai002/exp3$ git checkout -b"targetbranch"
Switched to a new branch 'targetbranch'
git@ise:~/1mv23ai002/exp3$ gedit file1.txt
git@ise:~/1mv23ai002/exp3$ git stash apply
Auto-merging file1.txt
CONFLICT (content): Merge conflict in file1.txt
git@ise:~/1mv23ai002/exp3$ git add file1.txt
git@ise:~/1mv23ai002/exp3$ git commit -m "file1 updated successfully"
[targetbranch 5b81dbd] file1 updated successfully
 1 file changed, 4 insertions(+)
git@ise:~/1mv23ai002/exp3$ gedit file1.txt
git@ise:~/1mv23ai002/exp3$ git checkout master
Switched to branch 'master'
git@ise:~/1mv23ai002/exp3$ gedit file1.txt
git@ise:~/1mv23ai002/exp3$ git merge "targetbranch"
Updating 92f9523..5b81dbd
Fast-forward
 file1.txt | 4 ++++
 1 file changed, 4 insertions(+)
git@ise:~/1mv23ai002/exp3$ gedit file1.txt
git@ise:~/1mv23ai002/exp3$ git branch --list
* master
  sourcebranch
  targetbranch
git@ise:~/1mv23ai002/exp3$ git stash list
stash@{0}: On sourcebranch: file1 modified
git@ise:~/1mv23ai002/exp3$ git stash drop stash@{0}
Dropped stash@{0} (3b50d447af33e91a704730e818db325395394591)
git@ise:~/1mv23ai002/exp3$
