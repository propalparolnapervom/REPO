## GIT ADD BRANCH LOCALLY TO YOUR FORKED REPO

### BRANCH OVERALL INFO

Git repositories use branches to isolate work when needed. 

It's common practice when working on a project or with others on a project to create a **branch** to keep your working changes in. This way you can do your work while the main, commonly named 'master', branch stays stable. When the work on your branch is finished you merge it back into the 'master' master branch.

> For a great visualization on how branches work in a project, see this [GitHub Guide](http://guides.github.com/overviews/flow)

When you create a branch, Git copies everything from the current branch you're on and places it in the branch you've requested be made.


### BRANCH ADDING TO LOCAL "patchwork" FORKED REPO

**1. Create a branch**

Go to the local forked repo
```
cd patchwork
```

See on what branch you're currently on
```
git branch

      * gh-pages
      
      
git status

      On branch gh-pages
      Your branch is up to date with 'origin/gh-pages'.

      nothing to commit, working tree clean
```

**Create a new branch**
Branches are case-sensitive.
```
git branch add-propalparolnapervom
```

**View available branches and your current one**
```
git branch

        add-propalparolnapervom
      * gh-pages
```

**To go into specific branch and work on it**
```
git checkout add-propalparolnapervom

      Switched to branch 'add-propalparolnapervom'
```

**View available branches and your current one**
```
git branch

      * add-propalparolnapervom
        gh-pages
```


**2. Create a new file**

Go to the following dir in ``patchwork`` locally forked repo
```
cd CONTRIBUTORS
```

Create a new file named ``add-propalparolnapervom.txt``.
  
Then, just write your GitHub username in it.



**3. Check-in**

See previously modified file
```
git status

      On branch add-propalparolnapervom
      Untracked files:
        (use "git add <file>..." to include in what will be committed)

              add-propalparolnapervom.txt

      nothing added to commit but untracked files present (use "git add" to track)
```

Add changes to commit
```
git add add-propalparolnapervom.txt
```

Commit changes
```
git commit -m "commit message"

      [add-propalparolnapervom fc71c6675d] commit message
       1 file changed, 1 insertion(+)
       create mode 100644 CONTRIBUTORS/add-propalparolnapervom.txt
```

View remote addresses for your local repo
```
git remote -v

      origin  https://github.com/propalparolnapervom/patchwork (fetch)
      origin  https://github.com/propalparolnapervom/patchwork (push)
      upstream        https://github.com/jlord/patchwork.git (fetch)
      upstream        https://github.com/jlord/patchwork.git (push)
```
      
Push your update to just created branch (``add-propalparolnapervom``) of your forked repo (``origin``) on GitHub:
```
git push origin add-propalparolnapervom

      Enumerating objects: 6, done.
      Counting objects: 100% (6/6), done.
      Delta compression using up to 4 threads.
      Compressing objects: 100% (3/3), done.
      Writing objects: 100% (4/4), 368 bytes | 368.00 KiB/s, done.
      Total 4 (delta 2), reused 0 (delta 0)
      remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
      To https://github.com/propalparolnapervom/patchwork
       * [new branch]            add-propalparolnapervom -> add-propalparolnapervom
```































