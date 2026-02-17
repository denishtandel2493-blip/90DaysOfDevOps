# Day-23 Challenge
## Branching Commands
      -      list all braches in your repo
      -      Create a new branch called feature-1
      -      Switch to feature-1
      -      Create a new branch and switch to it in a single command — **git checkout -b feature-2**
<img width="852" height="504" alt="image" src="https://github.com/user-attachments/assets/2b5b93f0-1286-4906-b88c-dc2c09ebb279" />
                
      To make a commit on a branch that does not exist on main, you need to
            Create and switch to new branch : git checkout -b feature-1
            Create a new file               : touch demo1.txt
            Stage the file                  : git add demo1.txt
            Commit the File                 : git commit -m "Added demo.txt file"

<img width="849" height="927" alt="image" src="https://github.com/user-attachments/assets/141d72ed-4335-486b-81c8-f71752f4f18b" />

## Push to GitHub
            Create a new repository on GitHub (do NOT initialize it with a README)
            -      Go to GitHub
            -      Click New repository
            -      Fill in:
                        .      Repo Name (Ex. my-project)
                        .      Chose Public or Private
            -      Do Not Check:
                        .      Add a README
                        .      Add .gitignore
                        .      Add license
            -      Click Create Repository
<img width="1818" height="527" alt="image" src="https://github.com/user-attachments/assets/1f4c25bd-7e08-44a6-bafe-e5216d6e7c40" />

            Connect your local Repo to the GitHub remote
            -      Go to my local project folder: cd /practice/my-project
            -      If not already initialized: git init
            -      Add files and commit:
                  .      git add .
                  .      git commit -m "Added file"
            -      Copy my repo URL from GitHub :  https://github.com/username/my-project.git
            -      Run This Command:  git remote add origin https://github.com/username/my-project.git
            -      Verify remote:      git remote -v
<img width="853" height="907" alt="image" src="https://github.com/user-attachments/assets/4560c87c-41c8-433f-aaeb-8989e5fd6f9d" />
##  Pull from GitHub
            Pulling from GitHub is a common operation that updates your local repository with changes from a remote repository
            Git, pull means, Download changes from remote repository and merge them into your current branch
<img width="852" height="323" alt="image" src="https://github.com/user-attachments/assets/c2c11567-4489-4bd7-8b1e-13677b6632a4" />
