# 3b-1 Bash Backup Scripting, Cron Jobs & Cloud Export
Lab Steps:
- Create test files and directories in /home/ubuntu/Documents


- Write a Bash script to recursively copy /Documents to /backup.
- Zip the backup with a filename based on current date using date and zip.


- Move the final backup zip into /home/ubuntu for easy access.
- Grant execute permissions: chmod 777 testscript.

- Move script to /usr/bin/ and test system-wide execution.

- Schedule cron to run the script hourly: edit /etc/crontab.


- Add an SCP command to transfer the backup to a cloud instance.
- Test key-based SSH access and accept remote host fingerprints if prompted.

# Reflection Questions










