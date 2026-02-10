Create Users
    
    Create users with home directories and passwords
<img width="619" height="505" alt="image" src="https://github.com/user-attachments/assets/009e51d6-9c30-499e-8cb6-4c4e13421d91" />

Create Groups

    Groups in Linux allow administrators to organize and control user access to various resources and files.
    #sudo groupadd developers
<img width="187" height="131" alt="image" src="https://github.com/user-attachments/assets/547129d3-bfdb-4836-b076-2ad9ebc3a20a" />

Assign Users to Gruops

    Adding Users to Groups Using this Command
    # sudo gpasswd -a user_name group_name
<img width="372" height="190" alt="image" src="https://github.com/user-attachments/assets/069f030f-0ed8-4c91-bcc1-59fe4c5fc712" />

Shared Directory and Set group Ownership

    Create a new directory and set the gruop ownership to developers using this command
    # sudo chgrp group_name file_name
<img width="555" height="305" alt="image" src="https://github.com/user-attachments/assets/2dfb19a6-a457-48e9-acb7-0eaaed63c139" />
    
    Set permissions to 775 (rwxrwxr-x) directory and create a file as tokyo and berlin user
<img width="660" height="456" alt="image" src="https://github.com/user-attachments/assets/bc87151b-ef26-43f5-8d1a-0eddee652f97" />



