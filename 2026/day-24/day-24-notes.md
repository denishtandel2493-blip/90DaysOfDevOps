# Day-24 Challenge
## Git Merge 
    Git merge is used to combine changes from one branch into another branch.
    Most commonly, you merge a feature-login branch into main branch.
    Suppose you worked on a branch called feature-login and now want to merge it into main branch
<img width="852" height="181" alt="image" src="https://github.com/user-attachments/assets/00dc4002-132a-4f22-bdbc-1272224fb847" />
<img width="858" height="451" alt="image" src="https://github.com/user-attachments/assets/b4d4ce0a-d98f-4970-88c0-ced7f63d2dca" />

      Create another branch feature-signup, add commits to it — but also add a commit to main before merging
      Merge feature-signup into main — what happens this time?
      -     Git will create a merge commit (3-way merge)
      -     feature-signup has new commits and main ALSO has a new commit
      -     Both branches moved forward independently
<img width="851" height="899" alt="image" src="https://github.com/user-attachments/assets/70e8a39b-c6a1-4af9-978a-68bf7ce37e9d" />
        
        A fast-forward merge happens when Git can move the branch pointer forward without creating a new merge commit.
        It occurs when the target branch has no new commits since the feature branch was created.

# Git Rebase
      Git Rebase is used to move (or replay) commits from one branch onto another base branch.
      Instead of creating a merge commit (like git merge), rebase rewrites history to keep it linear.
<img width="836" height="519" alt="image" src="https://github.com/user-attachments/assets/3a14bb92-d125-4f80-9acc-3ab4193aab95" />
        
        Switch to feature-dashboard and rebase it onto main
<img width="850" height="724" alt="image" src="https://github.com/user-attachments/assets/b2fb68d2-ab20-4e9c-b569-0b802cea4b9d" />

