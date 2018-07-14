# GIT COMMANDS

## CONFIGURATION

**Get version of installed GIT**
```
git --version

      git version 2.18.0.windows.1
```

**Configure GIT so it knows to associate your work to you**

Set your name
```
git config --global user.name "propalparolnapervom"
```

Set your email
```
git config --global user.email "propalparolnapervom@gmail.com"
```

## WORKING WITH REPO

**Turn Git on for a folder**

Go to the necessary empty dir and tell Git to initialize (start tracking) the folder you are now in
```
mkdir test_dir
cd test_dir
git init

      Initialized empty Git repository in D:/overall/git_space/test_dir/.git/
```

## WORKING WITH FILES IN THE REPO

**Add new file**

Use Git to see what changed in your repository
```
git status

      On branch master

      No commits yet

      Untracked files:
        (use "git add <file>..." to include in what will be committed)

              readme.txt

      nothing added to commit but untracked files present (use "git add" to track)
```

Add the file you just created so that it becomes a part of the changes you will commit (aka save) with Git
```
git add readme.txt
```

Commit those changes to the repository's history with a short (m) message describing the updates
```
git commit -m "Created readme"

      [master (root-commit) 329014a] Created readme
       1 file changed, 3 insertions(+)
       create mode 100644 readme.txt
```







