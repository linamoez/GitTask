# Git Task

## 1. Initialize the Repository
```bash
git init
git add .
git commit -m "initial commit"
```

## 2. Create and Switch Branches
```bash
git branch dev
git branch
git switch dev
git switch -c test
```

## 3. Connect to GitHub
```bash
git remote add origin git@github.com:linamoez/GitTask.git
git remote -v
ssh -T git@github.com
```

## 4. Push Branches
```bash
git push -u origin main
git push -u origin dev
git push -u origin test
```

## 5. Add and Commit Files
```bash
git add README.txt
git commit -m "Initial commit"

git add kk.txt
git commit -m "added"

git add test.txt
git commit -m "new"
```

## 6. View Commit History
```bash
git status
git log --oneline
git log
```

## 7. Merge Branches
```bash
git switch main
git merge dev
git merge test
git commit -m "div merge"
```

## 8. Delete Branches
```bash
git branch -d dev
git branch -d test

git push origin --delete dev
git push origin --delete test
```

## 9. Create and Push Tags
```bash
git tag -a v1.7 -m "version 1.7"
git tag -a v2.0 -m "version 1.7"
git push --tags
```

## 10. Add and Push an Image
```bash
git add .
git commit -m "photo"
git push
```

## Repository
![PHOTO](HORSE.jpg)
