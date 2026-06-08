# Day-42 Challenge
## GitHub-Hosted Runners
      GitHub-hosted runners are temporary virtual machines (VMs) that GitHub provides to execute your Actions workflows. 
      You don’t manage the infrastructure; GitHub starts a fresh runner for each job and disposes of it afterward.

    GitHub-Hosted Runner એ GitHub દ્વારા આપવામાં આવતી Virtual Machine (VM) છે, જેમાં તમારા GitHub Actions workflows run થાય છે.
    જ્યારે workflow trigger થાય છે, ત્યારે GitHub નવી VM બનાવે છે, job ચલાવે છે અને job પૂર્ણ થયા પછી VM delete કરી દે છે.

    મુખ્ય વિશેષતાઓ:-
        GitHub દ્વારા મેનેજ થાય છે      
        Server setup કરવાની જરૂર નથી.
        Maintenance અને updates GitHub કરે છે.
        Clean Environment :- દરેક job માટે નવી VM મળે છે., અગાઉના job નો data રહેતો નથી.
        Pre-installed Tools:- Git, Python, Java, Docker, અન્ય ઘણા tools પહેલેથી installed હોય છે.
        Multiple Operating Systems: Linux (Ubuntu) , Windows, macOS
        
##  Explore What's Pre-installed
    GitHub-hosted runners come with many commonly used tools and languages already installed. 
    This saves time because you don't need to install them every time your workflow runs.
    Commonly Pre-installed Software:-
      On ubuntu-latest, GitHub typically includes:  Git, Python, Node.js, npm, Java, Docker, .NET SDK, Go, Ruby, Rust, PowerShell
      
## Set Up a Self-Hosted Runner
      A Self-Hosted Runner is a machine that you manage yourself and connect to GitHub Actions. Instead of running workflows on GitHub's servers, workflows run on your own computer, VM, or server.

      Why Use a Self-Hosted Runner?
      1]      Access to internal/private networks
      2]      Use custom software or hardware
      3]      Run jobs on powerful servers
      4]      Use GPUs or specialized devices
      5]      Avoid GitHub-hosted runner limits

## 
