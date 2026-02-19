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

##  Squash Commit
        A squash commit combines all feature branch commits into one single commit before merging.
<img width="851" height="974" alt="image" src="https://github.com/user-attachments/assets/c99ceb26-161a-4fa6-822a-174e821ddfeb" />
<img width="860" height="939" alt="image" src="https://github.com/user-attachments/assets/7cb1667d-de9a-4897-8c7b-1e7d4e9a92e7" />

## Merge Commit
        A merge commit is created when you merge a branch normally.
<img width="864" height="1000" alt="image" src="https://github.com/user-attachments/assets/be049923-9b2e-4ec5-b1a1-d6eaaf671103" />
<img width="844" height="661" alt="image" src="https://github.com/user-attachments/assets/f971441c-742c-4e5a-a482-04067c708b71" />

## Git Stash
        You are working on feature-1 branch and 
            You modified some files
            You did NOT commit yet
            Suddenly you need to switch to master branch
        Git may not allow switching if changes conflict.
    error: Your local changes to the following files would be overwritten by checkout:
           Filename.txt
        Please commit your changes or stash them before you switch branches to Aborting
<img width="851" height="458" alt="image" src="https://github.com/user-attachments/assets/c30dbc50-70b1-426e-bffd-797451bf7ccb" />

## Cherry Picking
        Taking one specific commit from one branch. Applying it to another branch
<img width="850" height="84" alt="image" src="https://github.com/user-attachments/assets/5e474a41-65d9-4c6e-a238-ac1f4d3367a4" />
<img width="1226" height="968" alt="image" src="https://github.com/user-attachments/assets/e915f269-b5f0-48c7-b85c-9f3ee919fb7d" />


