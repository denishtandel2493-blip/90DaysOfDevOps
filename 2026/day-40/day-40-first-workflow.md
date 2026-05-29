# Day-40 Challenge (Your First GitHub Actions Workflow)
## Set Up

<img width="1035" height="702" alt="image" src="https://github.com/user-attachments/assets/dea66e9a-721d-4a8b-ba02-d700511b2af4" />

## Hello Workflow
    If everything worked, the workflow status will be green.
<img width="1019" height="576" alt="image" src="https://github.com/user-attachments/assets/fc649c47-a5d8-4e24-9545-254d0ebc95eb" />

## Understand the Anatomy
    1] on:	Defines when the workflow should start (trigger). 
    2] jobs:	Contains all jobs/tasks the workflow will execute.
    3] runs-on:	Specifies which machine/OS will run the job. 
    4] steps:	List of actions or commands executed one by one inside a job.
    5] uses:	Uses a prebuilt GitHub Action from another repository.  
    6]run:	Executes shell commands directly on the runner machine.
    7] name: (step name)	Human-readable label shown in the Actions logs/UI.
    In Simple Gujarati:- 1] on:	Workflow ક્યારે ચાલશે. 
                         2] jobs:	શું કામ કરવાનું છે. 
                         3] runs-on:	કઈ machine પર run થશે.
                         4] steps:	એક પછી એક ચાલતા tasks. 
                         5] uses:	Ready-made GitHub Action ઉપયોગ કરવું.
                         6] run:	Command ચલાવવો. 
                         7] name: Step નું display નામ.
##  Add More Steps
<img width="1081" height="794" alt="image" src="https://github.com/user-attachments/assets/51071128-a63d-400a-a002-087164abac57" />

##  Break It On Purpose
    When a GitHub Actions pipeline fails, you will see:
       - Red ❌ status instead of green ✅
       - Workflow marked as Failed
       - Failed job/step highlighted in red
       - Execution stops at the failing step
<img width="1469" height="781" alt="image" src="https://github.com/user-attachments/assets/3f00152c-4878-4738-a5a0-45849d58fb41" />


