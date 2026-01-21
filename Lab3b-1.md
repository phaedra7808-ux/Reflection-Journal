# 3b-1 Bash Backup Scripting, Cron Jobs & Cloud Export
Lab Steps:
- Create test files and directories in /home/ubuntu/Documents
<img width="936" height="268" alt="image" src="https://github.com/user-attachments/assets/587bb064-7df6-47ca-9868-c21b137b175f" />


- Write a Bash script to recursively copy /Documents to /backup.
- Zip the backup with a filename based on current date using date and zip.
<img width="905" height="142" alt="image" src="https://github.com/user-attachments/assets/1a3b7abc-863e-4909-908c-0d64df847452" />
<img width="948" height="346" alt="image" src="https://github.com/user-attachments/assets/d526aee1-3d0b-49a3-ab5b-c66f9ec91d7b" />


- Move the final backup zip into /home/ubuntu for easy access.
- Grant execute permissions: chmod 777 testscript.
<img width="667" height="22" alt="image" src="https://github.com/user-attachments/assets/3bacdc35-e4a6-44b3-9e48-9df81cc28070" />

- Move script to /usr/bin/ and test system-wide execution.
<img width="472" height="46" alt="image" src="https://github.com/user-attachments/assets/12972f20-0896-49f9-943d-3ce7b89cc57e" />

- Schedule cron to run the script hourly: edit /etc/crontab.
<img width="532" height="55" alt="image" src="https://github.com/user-attachments/assets/bb1325e8-5cda-40fc-8a01-88eb0c12237c" />


- Add an SCP command to transfer the backup to a cloud instance.
- Test key-based SSH access and accept remote host fingerprints if prompted.

# Reflection Questions
- Why is using absolute paths important in scripts run by cron? 

Cron runs in a minimal environment that doesn't share your user's specific "shortcuts" (PATH), so absolute paths like /usr/bin/zip ensure the system finds the files every time.

- What are the benefits of cloud exporting for backups? 

Cloud exporting provides "off-site" redundancy, ensuring that if your primary server hardware fails or is deleted, your data remains safe and accessible in a separate location.

- How does cron differ from manual execution? 

Cron is an automated background service (daemon) that triggers tasks at scheduled times, whereas manual execution requires a user to be logged in and physically type the commands.

- What happens if SSH keys are not accepted ahead of time? 

The script will hang indefinitely while waiting for a user to type "yes" to accept the host fingerprint, causing the automated backup to fail.

- How can login messages help improve user/system engagement?

Custom login messages (MOTD) can inform users of recent backup successes, pending system maintenance, or security policies the moment they log into the server.









