# Day-44 Challenge
## GitHub Secrets
    Step 1: Create the Secret
    Go to: Repository → Settings → Secrets and variables → Actions → New repository secret
    Create:-  Name: MY_SECRET_MESSAGE
              Value: Hello Secret
<img width="581" height="380" alt="image" src="https://github.com/user-attachments/assets/5fded6ac-9fed-4abf-8115-7c91641e62ce" />
<img width="1262" height="643" alt="image" src="https://github.com/user-attachments/assets/9a710c4b-c989-44f7-a6df-a74b47c6a856" />

## Use Secrets as Environment Variables
    GitHub Secrets can be passed to your workflow as environment variables and then used by scripts or applications.
    Reads the GitHub Secret MY_SECRET_MESSAGE.
    Stores it in the environment variable MY_SECRET.
    Makes it available inside the script as $MY_SECRET.
    Secrets often contain sensitive information such as API keys, passwords, and access tokens, so they should never be exposed in CI/CD logs.
<img width="584" height="373" alt="image" src="https://github.com/user-attachments/assets/d2a3683f-71f3-4a6e-aba0-65cbb2b40391" />
<img width="1680" height="623" alt="image" src="https://github.com/user-attachments/assets/d13a64bd-fa77-4faa-ac26-a661507ebab5" />

## Upload Artifacts
    Artifacts are files generated during a workflow run (such as logs, test reports, build outputs, or packages) that can be stored on GitHub and downloaded later
    1] Save test reports 2] Store build outputs 3] Keep logs for troubleshooting 4] Share files between workflow jobs
    5] Download generated files after a workflow run without committing them to the repository
<img width="899" height="422" alt="image" src="https://github.com/user-attachments/assets/23ed7ecc-394a-474f-8f7c-977a023e5eec" />
<img width="1860" height="816" alt="image" src="https://github.com/user-attachments/assets/fe824741-5189-40ee-9200-82d1e1e6031c" />

## Run Real Tests in CI
        actions/checkout downloads your code.
        Dependencies are installed (Python in this example).
        The script is executed in CI.
        Any non-zero exit code causes the job to fail.
        Fixing the problem makes the pipeline pass again.
        
        This is the basic CI cycle used in real projects:
        Code Change → Push → CI Runs → Fail/Fix → CI Passes.
<img width="1619" height="919" alt="image" src="https://github.com/user-attachments/assets/a4517a1f-3952-4c0f-af43-d65b843ee4ef" />

    
