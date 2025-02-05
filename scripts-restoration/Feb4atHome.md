
欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$ cd ..

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop
$ git clone https://github.com/Shuqi-Ouyang/Botany563-classfiles.git
Cloning into 'Botany563-classfiles'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 10 (delta 0), reused 4 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (10/10), done.

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop
$ cd Botany564-classfiles
bash: cd: Botany564-classfiles: No such file or directory

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop
$ cd Botany563-classfiles

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ notepad notebook-log.md

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ notepad .gitignore

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ git add .

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ git commit -m"Add notebook-log.md and .gitignore"
[main 4a6060a] Add notebook-log.md and .gitignore
 2 files changed, 146 insertions(+)
 create mode 100644 .gitignore.txt
 create mode 100644 notebook-log.md

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 22 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 980 bytes | 980.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Shuqi-Ouyang/Botany563-classfiles.git
   a5558a5..4a6060a  main -> main

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ touch .gitignore

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ git add .

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ git commit -m"Update .gitignore"
[main b4098dc] Update .gitignore
 2 files changed, 146 deletions(-)
 create mode 100644 .gitignore
 delete mode 100644 .gitignore.txt

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 22 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 235 bytes | 235.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Shuqi-Ouyang/Botany563-classfiles.git
   4a6060a..b4098dc  main -> main

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ cd ..

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop
$ cd phylogenetics-class

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ cd ..

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop
$ git clone https://github.com/Shuqi-Ouyang/phylogenetics-class.git
Cloning into 'phylogenetics-class'...
remote: Enumerating objects: 2101, done.
remote: Counting objects: 100% (306/306), done.
remote: Compressing objects: 100% (168/168), done.
remote: Total 2101 (delta 185), reused 233 (delta 138), pack-reused 1795 (from 1)
Receiving objects: 100% (2101/2101), 245.43 MiB | 6.15 MiB/s, done.
Resolving deltas: 100% (1274/1274), done.

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop
$ cd phylogenetics-class

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git add .

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git commit -m"add Shuqi's repository link"
[master f7fe2b6] add Shuqi's repository link
 1 file changed, 1 insertion(+)

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git remote
origin

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git remote -v
origin  https://github.com/Shuqi-Ouyang/phylogenetics-class.git (fetch)
origin  https://github.com/Shuqi-Ouyang/phylogenetics-class.git (push)

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git remote add upstream https://github.com/crsl4/phylogenetics-class.git

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git remote -v
origin  https://github.com/Shuqi-Ouyang/phylogenetics-class.git (fetch)
origin  https://github.com/Shuqi-Ouyang/phylogenetics-class.git (push)
upstream        https://github.com/crsl4/phylogenetics-class.git (fetch)
upstream        https://github.com/crsl4/phylogenetics-class.git (push)

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git add .

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git add .

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git commit -m"add Shuqi's repository link"
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 22 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 453 bytes | 453.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Shuqi-Ouyang/phylogenetics-class.git
   41a2dc1..f7fe2b6  master -> master

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylogenetics-class (master)
$ cd ..

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop
$ cd Botany563-classfiles

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles (main)
$ cd scripts-restoration

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles/scripts-restoration (main)
$ add .
bash: add: command not found

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles/scripts-restoration (main)
$ ^C

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles/scripts-restoration (main)
$ ^C

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/Botany563-classfiles/scripts-restoration (main)
$