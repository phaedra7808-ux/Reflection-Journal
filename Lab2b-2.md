# 2b-2 Introduction to Bash Scripting & System Automation
Part 1: Navigating the File System and Managing Files
Students will: 
- Create and navigate directories 
- Use file commands to create, copy, rename, and delete files
<img width="783" height="146" alt="image" src="https://github.com/user-attachments/assets/f13a5ad2-a16d-4a75-9613-496de9d6f122" />


Part 2: Creating and Executing Basic Bash Scripts
Example: hello_world.sh
- Add #!/bin/bash
- Use echo to display messages
- Use chmod 777 to make the script executable
- Execute with ./hello_world.sh
<img width="883" height="107" alt="image" src="https://github.com/user-attachments/assets/09f56957-f5ca-4735-ad91-424dbd2b4c8e" />


Part 3: Implementing Loops and Conditionals
Example: system_info.sh
- Use for loop for countdowns or iteration
- Use if, elif, else to evaluate user input
- Use read for interactive input
<img width="517" height="413" alt="image" src="https://github.com/user-attachments/assets/b7874406-fb7a-48ee-ad42-8988e67684d9" />


Part 4: Automating System Monitoring Tasks
Example: resource_monitor.sh 
- Use top, free -h, df -h to monitor system resources
<img width="937" height="957" alt="image" src="https://github.com/user-attachments/assets/31242bb9-20b1-41f0-b9b9-9e6ae08864b8" />

- Use sleep and iteration input to control monitoring frequency
<img width="772" height="622" alt="image" src="https://github.com/user-attachments/assets/18a67aaa-5f83-4083-ad46-0fd8edbd0162" />


# Reflection Questions
- What command did you use to create a new directory?

I used the mkdir (make directory) command followed by the desired folder name.

- How can you view the contents of a file without opening it in a GUI?

You can use terminal commands like cat to display the whole file, or less and more to scroll through the content.

- What is the purpose of chmod 777? 

It grants full read, write, and execute permissions to the owner, the group, and all other users on the system.

- What does #!/bin/bash do at the start of a script? 

Known as a "Shebang," it specifies the path to the Bash interpreter that the system should use to execute the script's commands.

- What happens when invalid input is entered into a script? 

If not handled by an else statement or input validation, the script may produce errors, skip logic blocks, or terminate unexpectedly.

- What output does free -h show? 

It displays the total, used, and available system memory (RAM) in a human-readable format like MB or GB.

- How would you monitor network bandwidth in a Bash script? 

You could use a command like sar -n DEV or ifstat within a loop to capture and display real-time network traffic statistics.



