# GIT COMMANDS

## OVERALL

[Visual reference](http://marklodato.github.io/visual-git-guide/index-en.html)

[Docs #1](https://git-scm.com/book/ru/v1/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5)


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

Add GitHub Personal Access Token to the '~/.git-credentials' file (thus, don't ask it each time)
```
git config --global credential.helper store

# This time it doesn't show anything.
# Next time you commit/pull/etc it will ask github_username and github_token as usual
# Once you entered this credentials, it saves it to '~/.git-credentials' file (in a plane text!!!)
# All next times it doesn't ask you for credentials (it uses saved ones)
```

**View current global configs**

```
git config --list
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

**1. Push changes**
```
git push <REMOTENAME> <BRANCHNAME>
```

**2. Pull in changes**
```
git pull <REMOTENAME> <BRANCHNAME>
```

**See changes to the remote before you pull in**
```
git fetch --dry-run
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


## WORKING WITH BRANCHES

**View available branches**
```
git branch

      * master
```

**See on what branch you're currently on**
```
git status

      On branch gh-pages
      Your branch is up to date with 'origin/gh-pages'.

      nothing to commit, working tree clean
```

**Create a new branch**

Branches are case-sensitive.
```
git branch <BRANCHNAME>
```

**Delete branch in local repo**
```
git branch -d <BRANCHNAME>
```

**Delete branch in remote repo**
```
git push <REMOTENAME> --delete <BRANCHNAME>
```

**To go into specific branch and work on it**
```
git checkout <BRANCHNAME>
```

**Rename a branch you're currently on**
```
git branch -m <NEWBRANCHNAME>
```

**Checkout remote branch**

Checkout master
```
git clone -v <REPO>
```

Ckeckout it's branch
```
cd <REPO>
git checkout --track origin/<REMOTE_BRANCH_NAME>
```

**Resolving merge conflicts**

You have pushed the branch to the GitHub and turned out it can't be rebased and merged due to conflicts.

On your local PC.
```
cd <REPO>

# Make sure you have latest master version
git checkout master
git pull

# Start rebase process
git checkout <REMOTE_BRANCH_NAME>
git rebase master

# See files that could be added with and without a conflict
git status

# Manually update all files with conflicts (by editing it via any editor to the state you think should be)

# Once all files with conflicts are updated, mark it as resolved ones
git add <your_files>

# Continue rebase process
git rebase --continue

      Applying: iam, iamdelegate: Access from local PC to the openocean-documents-integration-secretly-guiding-sculpin s3 bucket was added

# Without any commits, you're should be clear now. Check it by
git status

      On branch DEVOPS-1706_access_to_doc_bucket_integr
      nothing to commit, working tree clean
      
# Push resolved conflicts to the GitHub
git push origin <REMOTE_BRANCH_NAME> --force-with-lease

# Your PR should be updated in GitHub

# Re-request approves 

# Done

```


## WORKING WITH TAGS

[Tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging)

### LIST

All current tags
```
git tag
```

Latest tag
```
git describe --abbrev=0
```

### ADD

Add tag to existing commit (local repo)
```
git tag -a v1.0.1 -m "Fixed feature W" 4f98fb15535d1932a5cf59d3a9d66cef51ea4244
```

Add tag to existing commit (remote repo)
```
      #Tag existing commit
      
git tag -a v1.0.1 -m "Fixed feature W" 4f98fb15535d1932a5cf59d3a9d66cef51ea4244

      #Push it upstream
      
git push origin v1.0.1
```

### REMOVE

Remove tag from repo (local)
```
git tag --delete tagname
```

Remove tag from the repo (remote)
```
git push --delete origin tagname
```

### DOWNLOAD 

**Download code with specific tag**

Clone whole repo
```
git clone ...
```

List exsiting tags
```
git tag -l
```

Now you can checkout a specific tag:

(you will be on a branch named after the revision number of tag - so probable use next step instead)
```
git checkout tags/<tag_name>
```

OR: checkout and create a branch 
```
git checkout tags/<tag_name> -b <branch_name>
```



## LOGS

[Look at logs](https://www.atlassian.com/git/tutorials/git-log)

**View repo logs**

Overall
```
git log

      commit 487ccc2e8d24ce5cfaa2dfd19b8199052dc2ca79 (HEAD -> master, origin/master, origin/HEAD)
      Author: Sergii Burtovyi <sbur@Sergiis-MacBook-Pro.local>
      Date:   Thu Nov 15 16:23:11 2018 +0200

          DEVOPS-338: Upgrade nginx to latest alpine image
```

With tags
```
git log --decorate

      commit 487ccc2e8d24ce5cfaa2dfd19b8199052dc2ca79 (HEAD -> master, origin/master, origin/HEAD)
      Author: Sergii Burtovyi <sbur@Sergiis-MacBook-Pro.local>
      Date:   Thu Nov 15 16:23:11 2018 +0200

          DEVOPS-338: Upgrade nginx to latest alpine image
```

With tags, in line
```
git log --oneline --decorate

      ef083207b itinerary: fix: hide edit button
      442e25f39 itinerary: fix: hide details modal
      362bfeb46 (tag: port-v0.6.0) port: fix: sizeme version downgraded to a stable one
```



**Search**

Search specific word in the log in the commit message
```
git log --grep="CSR"
```
















