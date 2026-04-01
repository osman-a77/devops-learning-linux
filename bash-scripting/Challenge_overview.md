# Core Bash Scripting Challenges

**In this bash-scripting file I've included the solutions to 4 bash scripting challenges**

### Challenge 1: Basic Arithmetic Calculator

This script prompts user for two integer inputs, performs four basic arithmetic operations and then outputs solutions.

### Challenge 2: File Operations Script

This script automates creating a directory (bash_demo), a text file (demo.txt), writes a message with the current date into the file, and displays its contents.

### Challenge 3: File Checker with Permissions

This script prompts the user for a filename, checks if the file exists, and reports whether it is readable, writable, and executable.

### Challenge 4: Backup Script for Text Files

This script prompts the user for a source directory, creates a timestamped backup directory, copies all .txt files into it, and displays the number of files backed up.


## Key Learnings

1. How to create directories and files dynamically with mkdir and touch.
2. Using conditional statements (if, [ ]) to check file existence and permissions.
3. How to prompt user input with read and read -p.
4. Handling timestamps for unique backup directories using the date command.
5. Counting files and managing paths safely with quoted variables to handle spaces.


## Challenges Overcome

1. Ensuring the backup script worked even when directories or filenames contained spaces or special characters.
2. Fixing syntax issues with variable expansion (e.g., ${backup}_$timestamp) and quoting paths solved the problem.


## Why Bash Matters in DevOps?

Bash scripting is essential for automating repetitive tasks, like backups, deployments, and log monitoring. It enables rapid, reliable system management without relying on manual GUI operations. Bash scripts integrate well with CI/CD pipelines, server provisioning, and monitoring tools, making DevOps workflows efficient and reproducible.


