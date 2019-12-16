# git


## develop
```
git branch develop
vim README.md
git commit -am "branch develop"
git push -u origin develop
```


## feature
```
git checkout -b feature develop
vim README.md
git commit -am "branch feature"

git checkout develop
git merge --no-ff feature
git push origin develop

git branch -d feature
```


## release
```
git checkout -b release-1.0 develop
vim README.md
git commit -am "branch release-1.0"


git checkout develop
git merge --no-ff release-1.0
git push origin develop

git checkout master
git merge --no-ff release-1.0
git push

git branch -d release-1.0

git tag -a v1.0 master
git push --tags
```