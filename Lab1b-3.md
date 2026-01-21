# 1b-3 File Search, Analysis & Archiving in Linux
- Explore contents: ls -l, tree, or use less to inspect a few files.
<img width="747" height="512" alt="image" src="https://github.com/user-attachments/assets/0e1ae69a-7506-4ee2-9c72-ad22c9e4e934" />


- Search for filenames: find ./Gutenberg -name "*.txt"
<img width="736" height="61" alt="image" src="https://github.com/user-attachments/assets/3c12d548-50c7-4dad-acba-5fda2e68e3c2" />

 - Search for strings: grep -r 'keyword' ./Gutenberg or use find -exec grep
<img width="841" height="41" alt="image" src="https://github.com/user-attachments/assets/c111a87f-8832-42e6-81e6-e29e9d6560ac" />

# Reflection Questions
- Which command-line tool was the most useful in solving the questions? 
grep was the most useful because it allowed me to quickly filter through the actual text content of hundreds of files to find specific information.

- How might these search tools help in cybersecurity investigations? 
These tools allow investigators to quickly scan through massive system logs to find specific IP addresses, timestamps, or unauthorized "strings" left behind by an attacker.

- How could scripting improve repetitive search tasks? 
Scripting allows us to automate complex search patterns, such as scheduled daily scans for sensitive data or specific error codes, without manual input.

- What limitations did you encounter using grep and find? 
A major limitation is that grep and find can be very slow when searching through massive directories, and they require exact syntax to avoid returning thousands of irrelevant results.



