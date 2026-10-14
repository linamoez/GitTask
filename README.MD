![horses](HORSE.jpg)
# Initialize Git
git init

# Check the current status
git status

# Create a file
"Hello Git" | Out-File README.txt

# Stage the file
git add README.txt

# Make the first commit
git commit -m "Initial commit"

# Create branches
git branch dev
git branch test

# Switch to a branch
git switch dev

# Test SSH authentication
ssh -T git@github.com

# Add the GitHub remote
git remote add origin git@github.com:linamoez/GitTask.git

# Check the remote URL
git remote -v
git remote set-url origin git@github.com:linamoez/GitTask.git
# Upload main
git push -u origin main

# Upload dev
git push -u origin dev

# Upload test
git push -u origin test

git switch dev
git add kk.txt
git commit -m "Add kk.txt"
git push origin dev

git switch test
git add test.txt
git commit -m "Add test.txt"
git push origin test


# Switch to main
git switch main

# Merge dev into main
git merge dev

# Merge test into main
git merge test

# Push merged changes to GitHub
git push origin main


# Delete local branches
git branch -d dev
git branch -d test

# Delete remote branches from GitHub
git push origin --delete dev
git push origin --delete test

git push --origin delete dev
git push origin --delete dev

# Create annotated tags
git tag -a v1.7 -m "Version 1.7"
git tag -a v2.0 -m "Version 2.0"

# List all tags
git tag

# Push all tags to GitHub
git push origin --tags

git push origin v1.7

