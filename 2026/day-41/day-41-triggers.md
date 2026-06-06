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
<img width="608" height="421" alt="image" src="https://github.com/user-attachments/assets/149644e5-5cfa-4dc6-af76-dbf36e9b682e" />
        
        Can you trigger it manually and see your input printed ?
                No, I can't trigger workflows in your GitHub repository, 
                but you can run it from the Actions → Run workflow button and verify the input is printed in the logs
##  Matrix Builds
        A Matrix Build lets you run the same job multiple times with different configurations 
        (such as different operating systems, programming language versions, or environments)
<img width="1860" height="779" alt="image" src="https://github.com/user-attachments/assets/31999a55-6355-47e3-8916-1875387e5320" />

##  Exclude & Fail-Fast
    1] Exclude
            The exclude keyword is used to remove specific combinations from a matrix
            Example:
                    strategy:
                      matrix:
                        os: [ubuntu-latest, windows-latest]
                        python-version: ["3.10", "3.11"]
                    
                        exclude:
                          - os: windows-latest
                            python-version: "3.10"
            The combination windows-latest + Python 3.10 is excluded and will not run
    2] Fail-Fast
            fail-fast controls what happens when one matrix job fails.
            If any matrix job fails, GitHub Actions cancels the remaining running or queued matrix jobs to save time and resources.                
                Example :    
                    strategy:
                      fail-fast: true
                      matrix:
                        python-version: ["3.10", "3.11", "3.12"]

            To allow all matrix jobs to finish even if one fails

    Exclude: Removes unwanted matrix combinations.
    Fail-Fast: true: Stops other matrix jobs when one fails.
    Fail-Fast: false: Allows all matrix jobs to run to completion, even if some fail.

