#  1b-2 Linux File Permissions and Group Access Control
Lab Setup and Instructions:
- Create users: sudo adduser alice, sudo adduser bob, sudo adduser mallory
<img width="1167" height="463" alt="image" src="https://github.com/user-attachments/assets/fbf0e4f3-41b9-4a31-adb2-49d8c99a0e25" />
<img width="1117" height="140" alt="image" src="https://github.com/user-attachments/assets/eb699c0a-6f66-49d4-9447-6b43edb0504e" />
<img width="1165" height="153" alt="image" src="https://github.com/user-attachments/assets/e2310aea-c9f0-444c-ab2f-2e1d498e339c" />

- Create a group: sudo groupadd sharedgroup
<img width="686" height="21" alt="image" src="https://github.com/user-attachments/assets/df328d96-2b6a-4e4c-acfa-654a16f26483" />

- Create a directory: sudo mkdir /home/shared
<img width="717" height="17" alt="image" src="https://github.com/user-attachments/assets/5636259f-b4b0-47c9-863f-357627ca8c1c" />

- Create ten files inside it: sudo touch /home/shared/file{1..10}
<img width="871" height="18" alt="image" src="https://github.com/user-attachments/assets/45e59923-c671-416a-9925-0dee50d49ebd" />

- Change group ownership: sudo chgrp -R sharedgroup /home/shared
<img width="826" height="17" alt="image" src="https://github.com/user-attachments/assets/87e387ee-bdf0-4be8-9471-83a372c419d5" />

- Add Alice and Bob to group: sudo usermod -aG sharedgroup alice, sudo usermod -aG sharedgroup bob.
<img width="792" height="40" alt="image" src="https://github.com/user-attachments/assets/bbd10fe2-41ba-4b49-8665-eb26678fdf6d" />

- Set directory permissions: sudo chmod -R 770 /home/shared
<img width="753" height="20" alt="image" src="https://github.com/user-attachments/assets/ca3ab58f-0318-4683-8dc8-adbb9e4d4088" />

- Override Bob's rights: sudo chmod 750 /home/shared/*
<img width="737" height="21" alt="image" src="https://github.com/user-attachments/assets/0c5b05ed-c33f-4b9a-99d3-1f60b0f9ee2a" />

- Remove Mallory from any group with access.

- Switch user: su - alice, su - bob, su - mallory; use whoami and ls -l /home/shared to verify access.
<img width="491" height="46" alt="image" src="https://github.com/user-attachments/assets/bb3839e5-5443-4cbb-834b-9f9c2c36b734" />

- Document findings and permission differences per user.
<img width="637" height="47" alt="image" src="https://github.com/user-attachments/assets/789468c9-893c-4afb-b950-aa965e15ee24" />
<img width="605" height="270" alt="image" src="https://github.com/user-attachments/assets/8a460e5f-f32a-440b-8614-642e9d60f4e0" />

# Reflection Questions
- How do Linux permissions differ from Windows ACL? 

Linux uses a standard UGO (User, Group, Other) model for simplicity, whereas Windows uses Access Control Lists (ACLs) for more granular, complex permission rules per individual user.

- What’s the effect of chmod 770 vs 750? 

770 grants full read, write, and execute rights to both the owner and the group, while 750 restricts the group to "read and execute" only, removing their ability to modify or delete files.

- What is the risk of adding users to the sudo group? 

Users in the sudo group gain "root" privileges, allowing them to bypass all security restrictions, delete system files, or compromise the entire server's integrity.

- Why is it important to verify with su and whoami? 

Using su and whoami allows an administrator to physically test and confirm that the permission boundaries are working correctly from the perspective of each specific user account.












