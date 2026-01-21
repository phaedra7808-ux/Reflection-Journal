# 2b-1 Cloud Web Server Deployment with Amazon EC2
Lab Setup and Execution:
- Log in to AWS EC2 Console and create a new Ubuntu 20.04 instance (free tier eligible).
- Name the security group 'ssh-and-web' and allow both SSH and HTTP traffic.

- Download key pair and save safely. Use this for SSH login via terminal.

- Connect to the VM using provided SSH command (ssh -i key.pem ubuntu@IP). • - Run sudo apt update and install Apache using sudo apt install apache2

- Access the server using its public IP in a browser (via HTTP)
<img width="825" height="688" alt="image" src="https://github.com/user-attachments/assets/77a939f1-bd94-4a61-a03b-728a280cd9b0" />

- Modify /var/www/html/index.html using nano and test the changes live

<img width="817" height="295" alt="image" src="https://github.com/user-attachments/assets/ac2aa983-6fac-4864-9208-861538bb86c1" />


# Reflection Questions
- What were the benefits of cloud deployment over local virtualisation?

Cloud deployment provides global accessibility, instant scalability, and eliminates the need for maintaining physical hardware or local resource allocation.

- How does Apache serve files, and how did you verify this?

Apache listens for HTTP requests on Port 80 and serves files from the /var/www/html directory; I verified this by entering the EC2 public IP into a web browser.

- What did you learn about file ownership and permissions?

I learned that files in the web directory are owned by the system, requiring sudo privileges to modify them to ensure unauthorized users cannot alter the website content.

- What risks are associated with leaving instances running?

Leaving instances running can lead to unexpected financial costs once free-tier limits are exceeded and increases the security "attack surface" for potential hackers.

- How would you explain the difference between DNS and /etc/hosts to a client?

DNS is a global, public "phonebook" for the entire internet, while the /etc/hosts file is a private, local list on a single computer used to override or bypass public DNS settings.




