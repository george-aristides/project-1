# Clone
git clone <link>

# Check Status of Local Repo 
git status

# Create Branch
git checkout -b branch-name

# Switch Branch
git checkout branch-name

# Set Branch as Upstream
git branch --set-upstream-to=origin/branch-name

# Check Upstream Path of Branch
git branch -vv

# Push Changes
## Add Files to Staging

### Individual Files
git add file1 file2

### All Changes
git add .

## Commit
git commit -m "commit message here"

## Pushing to Github

### On Upstream Branch
git push

### On a Local Branch Directly to dev (or another branch on github)
git push origin dev

# Pull 

## Upstream Branch
git pull

## Non-Upstream Branch (dev as example)
git pull origin dev

# Delete Local Branch
git branch -d branch-name





