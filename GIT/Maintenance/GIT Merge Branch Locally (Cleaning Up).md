## GIT MERGE BRANCH LOCALLY, DELETE IT, PULL FROM UPSTREAM


**Merge Locally**

1. View current branches
```
git branch

      * add-propalparolnapervom
        gh-pages
```

2. Move into the branch you want to merge into—in (this case, the branch ``gh-pages``).
```
git checkout gh-pages

      Switched to branch 'gh-pages'
      Your branch is up to date with 'origin/gh-pages'
```

3. Tell Git what branch you want to merge in
```
git merge add-propalparolnapervom

      Updating c02d67928c..fc71c6675d
      Fast-forward
       CONTRIBUTORS/add-propalparolnapervom.txt | 1 +
       1 file changed, 1 insertion(+)
       create mode 100644 CONTRIBUTORS/add-propalparolnapervom.txt
```

4. Tidy up by deleting your feature branch. Now that it has been merged you don't really need it around.
```
git branch -d add-propalparolnapervom

      Deleted branch add-propalparolnapervom (was fc71c6675d).
```

5. View current branches
```
git branch

      * gh-pages
```

6. You can also delete the branch from your remote on GitHub:
```
git push origin --delete add-propalparolnapervom

      To https://github.com/propalparolnapervom/patchwork
       - [deleted]               add-propalparolnapervom
```




**Pull from Upstream**

To pull from the original upstream:
```
git pull upstream gh-pages

      remote: Counting objects: 22, done.
      remote: Compressing objects: 100% (10/10), done.
      remote: Total 22 (delta 12), reused 16 (delta 8), pack-reused 0
      Unpacking objects: 100% (22/22), done.
      From https://github.com/jlord/patchwork
       * branch                  gh-pages   -> FETCH_HEAD
         c02d67928c..66d0f1045e  gh-pages   -> upstream/gh-pages
      Updating fc71c6675d..66d0f1045e
      Fast-forward
       CONTRIBUTORS/add-HiFiJenny.txt/HiFiJenny |  1 +
       index.html                               | 26 +++++++++++++-------------
       2 files changed, 14 insertions(+), 13 deletions(-)
       create mode 100644 CONTRIBUTORS/add-HiFiJenny.txt/HiFiJenny
```










