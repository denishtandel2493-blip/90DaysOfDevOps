# Git Commands Reference
## Setup & Config
    git init :- Initializes a new Git repository.

    git config :- Sets configuration values like your name and email.
        e.g.  git config --global user.name "Your Name"
              git config --global user.email "your@email.com"

    git clone :- Creates a copy of an existing repository.
        e.g.   git clone https://github.com/username/repository.git

## Basic Workflow
        git status :- Shows the current state of your working directory.

        git add :-    stages changes for the next commit.
            e.g. git add filename.txt
                 git add .
                 
        git commit :- Record staged changes in the repository history.
            e.g. git commit -m "Add new feature"
            
        git push :- Uploads local commits to aremote repository.
            e.g. git push origin main
            
        git pull :- Fetches and merges changes from a remote repository.
            e.g. git pull origin main

## Viewing Changes
        git log :- Shows commit history.
            e.g. git log

        git diff :- Shows differences between files or commits.
            e.g. git diff filename.txt

        git show :- Displays details about a specific commit.
            e.g. git show <commit-hash>

        
    
