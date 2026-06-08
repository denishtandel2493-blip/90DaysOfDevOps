# Day-43 Challenge
## Multi-Job Workflow
    A Multi-Job Workflow contains more than one job in the same workflow file. 
    Each job runs independently and can run in parallel or in a specific order.
    Then go to your repository's Actions tab and verify that the workflow runs with the jobs in the order: build → test → deploy.
<img width="1614" height="482" alt="image" src="https://github.com/user-attachments/assets/76778cfc-063a-4356-aca4-558c7de31524" />
        
        Yes, the Actions workflow graph shows the dependency chain: build → test → deploy, with each job running only after the previous one succeeds.
    
## 
