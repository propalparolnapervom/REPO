# GIT COMMANDS

## CONFIGURATION

**Get version of installed GIT**
```
git --version

      git version 2.18.0.windows.1
```

**Configure GIT so it knows to associate your work to you**

Set your name and check it
```
git config --global user.name "propalparolnapervom"


git config --global user.name

      propalparolnapervom
```

Set your email and check it
```
git config --global user.email "propalparolnapervom@gmail.com"


git config --global user.email

      propalparolnapervom@gmail.com
```

Add your GitHub username to your Git configuration and check it
```
git config --global user.username propalparolnapervom


git config --global user.username

      propalparolnapervom
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

**Clone remote repo to your local**

Clone (download) remote repo to your local PC
```
git clone <URLFROMGITHUB>
```

**Update repo**

**1. Pull in changes**
```
git pull <REMOTENAME> <BRANCHNAME>
```

**2. Push changes**
```
git push <REMOTENAME> <BRANCHNAME>
```

**Sho branches**
```
git branch

      * master
```


## WORKING WITH FILES IN THE REPO

**Add/Update the file**

1. Use Git to see what changed in your repository
```
git status

      On branch master

      No commits yet

      Untracked files:
        (use "git add <file>..." to include in what will be committed)

              readme.txt

      nothing added to commit but untracked files present (use "git add" to track)
```

2. Add ...

... the file you just created so that it becomes a part of the changes you will commit (aka save) with Git
```
git add readme.txt
```

OR

... all new/changed files in the repo
```
git add .
```

3. Commit those changes to the repository's history with a short (m) message describing the updates
```
git commit -m "Created readme"

      [master (root-commit) 329014a] Created readme
       1 file changed, 3 insertions(+)
       create mode 100644 readme.txt
```

**See changes btw your local file and the commited one**

If some changes were made to the file from the repo, show the diff
```
git diff

      diff --git a/readme.txt b/readme.txt
      index 915203c..06b685a 100644
      --- a/readme.txt
      +++ b/readme.txt
      @@ -1,3 +1,3 @@
       1
      -11
      -111
      \ No newline at end of file
      +111
      +1111
      \ No newline at end of file
```


## WORKING WITH REMOTE CONNECTIONS

**View remote addresses**
```
git remote -v

      origin  https://github.com/propalparolnapervom/test_dir.git (fetch)
      origin  https://github.com/propalparolnapervom/test_dir.git (push)
```

**Add remote connection**
```
git remote add <REMOTENAME> <URL>
```

**Set an URL to a remote connection**
```
git remote set-url <REMOTENAME> <URL>
```

















