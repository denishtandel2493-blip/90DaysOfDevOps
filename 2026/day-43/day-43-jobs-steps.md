# Day-43 Challenge
## Multi-Job Workflow
    A Multi-Job Workflow contains more than one job in the same workflow file. 
    Each job runs independently and can run in parallel or in a specific order.
    Then go to your repository's Actions tab and verify that the workflow runs with the jobs in the order: build → test → deploy.
<img width="1614" height="482" alt="image" src="https://github.com/user-attachments/assets/76778cfc-063a-4356-aca4-558c7de31524" />
        
        Yes, the Actions workflow graph shows the dependency chain:
        build → test → deploy, with each job running only after the previous one succeeds.
    
## Environment Variable
    Environment Variables are key-value pairs used to store configuration data (such as API URLs, usernames, or settings) 
    that can be accessed by jobs and steps in a GitHub Actions workflow.
<img width="1778" height="670" alt="image" src="https://github.com/user-attachments/assets/0a5b9107-b5b5-41f4-8c32-5fa2f0ac17de" />

##  Job Outputs
        Job Outputs are used to pass data from one job to another job in a GitHub Actions workflow.
        To share data generated in one job with another job.
        To avoid recalculating the same information multiple times.
        To pass build versions, artifact names, image tags, dates, or deployment URLs.
        To keep jobs independent while allowing them to exchange required information.
        Useful in CI/CD pipelines where a build job produces data that deployment or testing jobs need later.
<img width="1710" height="597" alt="image" src="https://github.com/user-attachments/assets/12b6bf8b-2ffa-40ac-8b0a-4b7175aa3005" />

## Conditionals
    Conditionals નો ઉપયોગ ત્યારે થાય છે જ્યારે કોઈ job અથવા step ને ચોક્કસ શરત (condition) સાચી હોય ત્યારે જ ચલાવવો હોય. તેના માટે if: keyword વપરાય છે.
<img width="1810" height="856" alt="image" src="https://github.com/user-attachments/assets/c60084f9-3374-4d08-b636-3c8d7ecc0379" />

## Putting It Together
    Create .github/workflows/smart-pipeline.yml that: Triggers on push to any branch  
        Has a lint job and a test job running in parallel
        Has a summary job that runs after both, prints whether it's a main branch push or a feature branch push, and prints the commit message
<img width="1858" height="629" alt="image" src="https://github.com/user-attachments/assets/4f3b9b5c-e3d6-48c1-bf92-0f920c051c3b" />


