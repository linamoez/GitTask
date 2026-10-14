# 1. Initialize Git and make the first commit
git init
git status
"Hello Git" | Out-File README.txt
git add README.txt
git commit -m "Initial commit"

# 2. Create and switch branches
git branch dev
git branch test
git switch dev
git branch
git switch -c feature

# 3. Set up SSH (only if you don't already have a key)
ls ~/.ssh
ssh-keygen -t ed25519 -C "your_email@example.com"
Get-Content ~/.ssh/id_ed25519.pub | Set-Clipboard
# Add the public key at https://github.com/settings/keys
ssh -T git@github.com

# 4. Connect to GitHub
git remote add origin git@github.com:linamoez/GitTask.git
git remote -v
# If origin already exists, use:
git remote set-url origin git@github.com:linamoez/GitTask.git

# 5. Push branches to GitHub
git push -u origin main
git push -u origin dev
git push -u origin test

# 6. Make changes and commit on dev
git switch dev
"Hello from dev" | Out-File kk.txt
git add kk.txt
git commit -m "Add kk.txt"
git push origin dev

# 7. Make changes and commit on test
git switch test
"Hello from test" | Out-File test.txt
git add test.txt
git commit -m "Add test.txt"
git push origin test

# 8. Stash changes to switch branches without committing
git stash -u
git switch main
git switch test
git stash pop
git stash list
git stash apply
git stash drop

# 9. Merge dev and test into main and push
git switch main
git merge dev
git merge test
git push origin main

# 10. Configure the Git editor if needed
git config --global core.editor "notepad"

# 11. Delete local and remote branches after merging
git branch -d dev
git branch -d test
git push origin --delete dev
git push origin --delete test

# 12. Create and push tags
git tag -a v1.7 -m "Version 1.7"
git tag -a v2.0 -m "Version 2.0"
git tag
git push origin --tags
git push origin v1.7

# 13. Add a photo and push
git add horse-herd-hierarchy-and-social-order-featured.webp
git commit -m "Add photo"
git push

# 14. Create a Git bundle for Google Drive
git bundle create GitTask.bundle --all
# Upload GitTask.bundle to Google Drive

# 15. Final verification
git status
git branch
git branch -r
git log --oneline --graph --decorate --all
git tag
git remote -v
git switch main
git push origin main