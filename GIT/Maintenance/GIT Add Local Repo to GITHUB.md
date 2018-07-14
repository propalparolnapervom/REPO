# GIT ADD LOCAL REPO TO GITHUB.md

## Overall GITHUB information

These are common files in open source projects so to make starting a new project easier, GitHub provides an option for creating them for you.

1. A **readme** explains what the project is, how to use it, and often times, how to contribute (though sometimes there is an extra file, 'CONTRIBUTING.md', for those details).

2. A **.gitignore** is a list of files that Git should not track, for instance, files with passwords!

3. A **license** file is the type of license you put on your project. This lets others know how they can use it. Information on the types is here: [choosealicense.com](https://choosealicense.com/)


## ADD LOCAL REPO "test_dir" TO GITHUB

### 1. Create a Remote Repository

1.1. Go to [github.com](https://github.com/), log in, and click the '+' in the top right and then click 'New repository'.

1.2. Give it a name that matches your local repository's name (test_dir) and a short description.

1.3. Make it public. This means it'll be listed on your public profile.

1.4. Don't initialize with a README because we already have a file, locally, named 'readme.txt'. This is a helper option from GitHub if you hadn't already made it.

1.5. Leave '.gitignore' and 'license' set to 'none'. We won't use them this tutorial.

1.6. Click create repository!


### 2. Connect your Local ("test_dir" on local PC) to your Remote ("test_dir" on GitHub)

At the top on just created empty GitHub repo there is 'Quick Setup' -> "HTTP" button -> Copy the addres (this is the address of your repo on GitHub's servers)
```
https://github.com/propalparolnapervom/test_dir.git
```

> Local repo can have multiple remotes so each requires a name. The primary remote is typically named ``origin``.

Add a remote named 'origin' to your local repo (have to be done from local repo)
```
cd test_dir
git remote add origin https://github.com/propalparolnapervom/test_dir.git
```


### 3. Push Work to your Remote
Next you want to push (send) everything you've done locally to your remote repository on GitHub.

Git has a branching system so that you can work on different parts of a project at different times. By default the first branch is named 'master'. When you push (and later pull) from a project, you tell Git the branch name you want and the name of the remote that it lives on.

So, send our branch named 'master' to our remote on GitHub named 'origin'.
```
git push origin master

      Enumerating objects: 6, done.
      Counting objects: 100% (6/6), done.
      Delta compression using up to 4 threads.
      Compressing objects: 100% (2/2), done.
      Writing objects: 100% (6/6), 412 bytes | 206.00 KiB/s, done.
      Total 6 (delta 1), reused 0 (delta 0)
      remote: Resolving deltas: 100% (1/1), done.
      To https://github.com/propalparolnapervom/test_dir.git
       * [new branch]      master -> master
```

Now go to your remote repository's page on GitHub.com and refresh the page. Wow! Everything is now the same locally as it is remotely.


























