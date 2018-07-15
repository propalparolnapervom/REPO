## GIT FORK REMOTE REPO

### FORK/CLONE OVERALL INFO

When you fork a repository, you're creating a copy of it on your GitHub account. Your forked copy begins its life as a remote repository—it exists just on your GitHub account, not on your computer. Forks are used for creating your own version of a project (this diversion from the original is like taking a fork in the road) or contributing back your changes (such as bug fixes or new features) to the original project.

To get a forked repository from your GitHub account onto your computer you clone it. This cloning action copies the remote repository onto your computer so that you can work on it locally.


### FORK "patchwork" REMOTE REPO

The test project to fork is at github.com/jlord/patchwork.

1. Go to the [project](https://github.com/jlord/patchwork) you want to fork 

2. Click the 'Fork' button at the top right. Once the forking animation is complete, you have a copy on your account.

3. Copy your fork's HTTP URL from the address bar in your browser, this is the address of your fork on GitHub's servers
```
https://github.com/propalparolnapervom/patchwork
```


### CLONE MY "patchwork" FORK

Clone your fork locally

1. Go to the any empty dir (create a new one) on your local PC (not in any other Git-repo!!!)
```
mkdir fork_test
cd fork_test
```

2. Clone your fork
```
git clone https://github.com/propalparolnapervom/patchwork

      Cloning into 'patchwork'...
      remote: Counting objects: 299754, done.
      remote: Compressing objects: 100% (41/41), done.
      remote: Total 299754 (delta 24), reused 29 (delta 9), pack-reused 299698
      Receiving objects: 100% (299754/299754), 113.72 MiB | 772.00 KiB/s, done.
      Resolving deltas: 100% (137084/137084), done.
      Checking out files: 100% (1027/1027), done.
```

3. Go into the folder it created for your local copy of the fork (in this case, named 'patchwork').
```
cd patchwork
```

4. See the address to the fork is already set up
```
git remote -v

      origin  https://github.com/propalparolnapervom/patchwork (fetch)
      origin  https://github.com/propalparolnapervom/patchwork (push)
```


## CONNECT TO HE ORIGINAL REPO

What if the original repo you forked happens to change? You'll want to be able to pull in those changes too. So let's add another remote connection, this time to the original, github.com/jlord/patchwork, repository with its URL.

You can name this remote connection anything you want, but typically people use the name 'upstream'; let's use that for this.
```
git remote add upstream https://github.com/jlord/patchwork.git
```

See the address to the fork
```
git remote -v

      origin  https://github.com/propalparolnapervom/patchwork (fetch)
      origin  https://github.com/propalparolnapervom/patchwork (push)
      upstream        https://github.com/jlord/patchwork.git (fetch)
      upstream        https://github.com/jlord/patchwork.git (push)
```

























