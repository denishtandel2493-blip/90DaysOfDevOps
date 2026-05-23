# Day-39 Challenge
## The Problem 
    Think about a team of 5 developers all pushing code to the same repo manually deploying to production
What can go wrong? 

    1] Developers overwrite each other’s code 2] Merge conflicts happen frequently 3] Wrong version gets deployed       
    4] Manual deployment mistakes occur
What does "it works on my machine" mean and why is it a real problem?

      “It works on my machine” means: The application works on the developer’s local system but fails on another system or production server.            
      This happens because environments are different: 1] Different OS versions 2] Different package versions 3] Missing dependencies
How many times a day can a team safely deploy manually?

    1] Very few times per day 2] Sometimes only once daily 3] Some teams deploy only weekly
    Why manual deployments are risky: 1] Human mistakes increase 2] Deployment takes longer
## CI vs CD
Continuous Integration 
        
        Continuous Integration is the practice of developers frequently merging code changes into a shared repository, often multiple times a day.
        Each change automatically triggers builds, tests, and code validation to catch bugs, merge conflicts, or broken code early.    
    Real-world example:
        A developer pushes code to GitHub, and GitHub Actions automatically runs unit tests and checks whether the application still builds successfully.
        
Continuous Delivery

        Continuous Delivery extends CI by automatically preparing the application for release after tests pass.
        The software is always kept in a deployable state, but deployment to production usually requires a manual approval step.
    Real-world example:
        After successful testing in Jenkins, a Docker image is built and deployed to a staging Kubernetes cluster, waiting for a team lead to approve production release.

Continuous Deployment

        Continuous Deployment goes one step beyond Continuous Delivery.
        Every change that passes automated testing is automatically deployed to production without human approval.
    Real-world example:
        A company like Netflix can automatically deploy small backend updates to production after all automated tests and monitoring checks pass.

    
        
    
