
欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~
$ cd desktop

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop
$ cd phylo-class-social

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$ git remote -v
origin  https://github.com/Shuqi-Ouyang/phylo-class-social.git (fetch)
origin  https://github.com/Shuqi-Ouyang/phylo-class-social.git (push)
upstream        https://github.com/crsl4/phylo-class-social.git (fetch)
upstream        https://github.com/crsl4/phylo-class-social.git (push)

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$ git pull upstream
remote: Enumerating objects: 28, done.
remote: Counting objects: 100% (18/18), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 28 (delta 16), reused 7 (delta 7), pack-reused 10 (from 1)
Unpacking objects: 100% (28/28), 6.15 KiB | 41.00 KiB/s, done.
From https://github.com/crsl4/phylo-class-social
   94b75ca..ca42c40  master     -> upstream/master
You asked to pull from the remote 'upstream', but did not specify
a branch. Because this is not the default configured remote
for your current branch, you must specify a branch on the command line.

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$ mkdir shuqi.md

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$ rmdir shuqi.md

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$ notepad shuqi.md

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$ git add .

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$ git commit -m "quiz"
[master c2a9979] quiz
 1 file changed, 1 insertion(+)
 create mode 100644 shuqi.md

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 22 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 310 bytes | 28.00 KiB/s, done.
Total 3 (delta 1), reused 1 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Shuqi-Ouyang/phylo-class-social.git
   451a80e..c2a9979  master -> master

欧阳葭@LAPTOP-5PMP3V9O MINGW64 ~/desktop/phylo-class-social (master)
$