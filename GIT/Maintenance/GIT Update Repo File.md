# GIT FILE UPDATING

**Update an existing file "VAGRANT Structure.xmind" in the master repo XMINDS**

1. Go to any empty dir on your local PC (or create a new one)
```
mkdir D:\overall\git_space
cd D:\overall\git_space
dir
```

2. Clone (download) a repo XMINDS from GitHub
```
git clone https://github.com/propalparolnapervom/XMINDS.git
```

3. Go to the just downloaded (cloned) repo dir and see necessary file
```
cd D:\overall\git_space\XMINDS\Tools\VAGRANT
dir

       Directory of D:\overall\git_space\XMINDS\Tools\VAGRANT

      14-Jul-18  14:21    <DIR>          .
      14-Jul-18  14:21    <DIR>          ..
      14-Jul-18  14:21           299,003 VAGRANT Structure.xmind
```

4. Update necessary file

5. See updated file as git
```
git status

      On branch master
      Your branch is up to date with 'origin/master'.

      Changes not staged for commit:
        (use "git add <file>..." to update what will be committed)
        (use "git checkout -- <file>..." to discard changes in working directory)

              modified:   VAGRANT Structure.xmind

      no changes added to commit (use "git add" and/or "git commit -a")
```

6. Add updated file to the downloaded repo
```
git add -A
git status

      On branch master
      Your branch is up to date with 'origin/master'.

      Changes to be committed:
        (use "git reset HEAD <file>..." to unstage)

              modified:   VAGRANT Structure.xmind
```

7. Commit updated file to the downloaded repo
```
git commit -a -m "Old file has been updated to the repo"

      [master 2c253a8] Old file has been updated to the repo
       1 file changed, 0 insertions(+), 0 deletions(-)
```

8. Place updated file to the master repo (from which local repo has been cloned initially)
```
git push

      Enumerating objects: 9, done.
      Counting objects: 100% (9/9), done.
      Delta compression using up to 4 threads.
      Compressing objects: 100% (3/3), done.
      Writing objects: 100% (5/5), 34.32 KiB | 4.29 MiB/s, done.
      Total 5 (delta 1), reused 0 (delta 0)
      remote: Resolving deltas: 100% (1/1), completed with 1 local object.
      To https://github.com/propalparolnapervom/XMINDS.git
         aedca82..2c253a8  master -> master
```


















