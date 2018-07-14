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
$ mkdir test_dir
$ cd test_dir
$ git init

      Initialized empty Git repository in D:/overall/git_space/test_dir/.git/
```

**Check the files status in the current repo**
```
$ git status
```
