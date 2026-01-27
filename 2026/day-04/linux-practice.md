Basic linux commands

CHECK RUNNING PROCESSES COMMAND

  - ``htop`` --> Display sorted information about processes with visual highlights. It allows you to scroll vertically and horizontally, so you can see every process running on your system and commands.

  <img width="1837" height="361" alt="image" src="https://github.com/user-attachments/assets/a874a5e3-47ca-4a93-88ff-7283af0400c0" />

   - ``kill`` --> Kill a process specified by its process ID PID, which you obtain using the ps command.

  <img width="471" height="116" alt="image" src="https://github.com/user-attachments/assets/a570db88-b9f1-4928-86c9-2473aaf7a9bb" />

SERVICE COMMAND

  - ``systemctl status sshd.service`` --> Displays the detailed status of a specific service, including whether it is active (running) or inactive (stopped), and recent log entries.

    <img width="779" height="244" alt="image" src="https://github.com/user-attachments/assets/1edc77dd-8239-4d75-af7b-e4eec63e4498" />

  
- ``systemctl list-units`` --> Shows a list of all active systemd units (services, mount points, sockets, etc.)

  <img width="1880" height="229" alt="image" src="https://github.com/user-attachments/assets/f63e4ed9-2fe1-4eb4-9300-30c29d6b3910" />

LOG COMMAND

- ``journalctl -u <service>`` --> On modern Linux systems using systemd, this command is used to view logs collected by the systemd journal. It offers robust filtering options by time, service, or priority.

  <img width="1887" height="126" alt="image" src="https://github.com/user-attachments/assets/43ac51f0-a3e8-4108-8214-8d99974cd7f6" />

  - ``tail -n 10 app.log`` --> Shows the last few lines of a file (10 lines by default). The -f option is invaluable for real-time monitoring of new entries as they are written.

   <img width="571" height="267" alt="image" src="https://github.com/user-attachments/assets/18f6b7cc-eb12-4132-bf06-0fddcc0f6fc1" />

  


  





  

  



  

