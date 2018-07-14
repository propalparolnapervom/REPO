# GIT MAINTENANCE

## WORKING WITH GITHUB

**Clone a repo XMINDS from GitHub**

1. Go to any empty dir (or create a new one)
```
mkdir D:\overall\git_space
cd D:\overall\git_space
dir
```

2. Clone the repo
```
git clone https://github.com/propalparolnapervom/XMINDS.git
```

**Add a new dir with file to the repo XMINDS**

1. Go to the downloaded (cloned) repo dir
```
cd D:\overall\git_space\XMINDS
```

2. Put (create) a necessary dir/file
```
dir 

       Directory of D:\overall\git_space\XMINDS

      14-Jul-18  14:06    <DIR>          .
      14-Jul-18  14:06    <DIR>          ..
      14-Jul-18  14:06    <DIR>          Tools
```

3. See new dir/file as git
```
git status

      On branch master

      No commits yet

      Untracked files:
        (use "git add <file>..." to include in what will be committed)

              Tools/

      nothing added to commit but untracked files present (use "git add" to track)
```

4. Add new dir/files to the downloaded repo
```
git add *
git status

      On branch master

      No commits yet

      Changes to be committed:
        (use "git rm --cached <file>..." to unstage)

              new file:   Tools/VAGRANT/VAGRANT Structure.xmind
```

5. Commit new dir/files to the downloaded repo
```
git commit * -m "New file has been added to the repo"

      [master (root-commit) 5828fd9] New file has been added to the repo
       1 file changed, 0 insertions(+), 0 deletions(-)
       create mode 100644 Tools/VAGRANT/VAGRANT Structure.xmind
```

6. Place new file to the master repo (from which local repo has been cloned initially)
```
git push

      Enumerating objects: 5, done.
      Counting objects: 100% (5/5), done.
      Delta compression using up to 4 threads.
      Compressing objects: 100% (3/3), done.
      Writing objects: 100% (5/5), 49.61 KiB | 7.09 MiB/s, done.
      Total 5 (delta 0), reused 0 (delta 0)
      To https://github.com/propalparolnapervom/XMINDS.git
       * [new branch]      master -> master
```


















