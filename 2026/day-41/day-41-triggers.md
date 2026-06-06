# Day-41 Challege Triggers & Matrix Builds
## Trigger on Pull Request
    A Pull Request (PR) trigger in GitHub Actions means that a workflow runs automatically whenever a Pull Request is created, updated, or modified.
      Example:    on:
                    pull_request:
                      branches:
                        - main    
<img width="629" height="454" alt="image" src="https://github.com/user-attachments/assets/0637e778-7671-45f5-bec8-2dbe929d9d98" />

## Scheduled Trigger
    A Scheduled Trigger allows a workflow to run automatically at specific times, just like a cron job in Linux.
    To run a GitHub Actions workflow every day at midnight UTC, add a schedule trigger like this
    Example:  on:
                schedule:
                  - cron: '0 9 * * 1'
        Cron expression for every Monday at 9:00 AM (UTC): 0 9 * * 1

## Manual Trigger 
        allows you to start a workflow yourself from the GitHub web interface instead of waiting for a push, pull request, or schedule.
