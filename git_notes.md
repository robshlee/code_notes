**delete branch locally**  
git branch -d localBranchName

**delete branch remotely**  
git push origin --delete remoteBranchName

**create new branch**  
git checkout -b [name_of_branch]

**push created branch to github**  
git push origin [name_of_branch]

**force pull and overwrite**  
git fetch --all
git reset --hard origin/<branch_name>