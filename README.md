# Automated User Provisioning With Bash


Hello, my name is Bryan Iheanacho and in this guide I will explain how to use automation to simplify and streamline user provisioning tasks in IT environments. By leveraging a Bash script, we will efficiently create user accounts, assign group memberships, and implement security policies with minimal manual intervention.

---

## Features

1. Automates:
- User account creation.
- Home directory setup and default shell configuration.
- Password assignment and expiration enforcement for first login.
- Group membership assignment.

2. Reads user information from a CSV file.

3. Logs operations for transparency and troubleshooting.

4. Optional: Sends email notifications to provisioned users.

---

### Step 1: Understand the Requirements
Before you begin, ensure you have:

1. A Linux machine with Bash installed.
2. Superuser (root) privileges.
3. A text editor such as nano, vim, or gedit for creating the script.
4. A basic understanding of Linux commands like useradd, chpasswd, passwd, and usermod.

---

### Step 2: Create the Bash Script
1. Open a terminal.
2. Create a new script file:
   - vim provision_users.sh 
   - Add the needed bash script content to the file
   - Save the file and exit the editor using **ESC** and **:wq!**
     
![autoUser-provision1-bashpic1](https://github.com/user-attachments/assets/087251ea-d264-4d02-ab76-4709321f49a4)
![autoUser-provision1-bashpic2](https://github.com/user-attachments/assets/eff37c53-51ee-4177-866f-59da905efde1)

---

### Step 3: Create the CSV File  
1. Create a new  file:
   - vim users.csv 
   - Add the needed sample content to the file (in **username,full_name,email** form)
   - Save the file and exit the editor using **ESC** and **:wq!**
     
![autoUser-provision1-CSV-file1](https://github.com/user-attachments/assets/7bbabdbb-391b-4a4e-8e43-8e62d726ec7c)

---

### Step 4: Make the Script Executable
1. Grant the execute permissions to the script:
   - **chmod +x provision_users.sh**

---

## Step 5 Execute the Script
1. Run the script with superuser privileges:
   - sudo **./provision_users.sh**

---

## Validate Results
Results After Running the Script
Below are the results of executing the Bash script. The script successfully reads the content from the users.csv file we created. It processes each entry to:
- Create the user account.
- Assign the user to the default group developers.
- Associate the specified email with the user account.

Additionally, the script ensures that the passwords for the newly created users are set to expire upon their first login, prompting them to set a new password.

![autoUser-provision1](https://github.com/user-attachments/assets/9201109c-4b28-41cc-8cb8-267552c7731b)

---

### Conclusion
This project demonstrates how automation can simplify and streamline user provisioning tasks in IT environments. By leveraging a Bash script, we efficiently created user accounts, assigned group memberships, and implemented security policies with minimal manual intervention.

This script provides a foundation for further enhancements, such as integrating unique password generation, email notifications, or even extending it to work in multi-platform environments.

I hope this project serves as a helpful guide for automating repetitive administrative tasks and inspires you to explore more possibilities in Linux scripting and IT automation.

Thank you for exploring this project!
