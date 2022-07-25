## Introduction to Scripting

In this activity, you are a junior administrator at Rezifp Pharma Inc. 

- It is your responsibility to ensure the security of the organization’s network by automating many tasks, such as moving patient data files, from various locations using `cron`. 

- Many of these tasks are accomplished through automation, using scripts written to run at regular intervals or as periodically as determined by your department. 

- In response to malware, adware, and virus attacks, your organization has asked you to ensure proper configuration management of all networking equipment and associated systems. 

- In addition to the threat of malware and attacks, portions of the Health and Portability Act (HIPAA), require organizations to maintain a regular backup regimen for the safe and secure storage of patient data. In response to HIPAA regulations, your organization also ensures that any unused, temporary, and cached files are removed regularly.

You have been tasked to:

- Create a script, `backup.sh`, that creates a backup of the system's `/home` directory.

- Create a script, `update.sh`, that upgrades packages to their most recent version, keeping the system up-to-date.

- **Bonus:** Create a script, `cleanup.sh`, that removes any unused, temporary, and cached files.

- Test the scripts by running them with bash, using the `sudo ./<name of the script>.sh` command.

### Instructions

1. Begin by creating a directory to hold your scripts in `~/Security_scripts`. Then, move into this directory.

2. Create a script file called `backup.sh` that does the following:

        #!/bin/bash

        # Create /var/backup if it doesn't exist
        mkdir -p /var/backup

        # Create new /var/backup/home.tar
        tar cvf /var/backup/home.tar /home

        # Moves the file `/var/backup/home.tar` to `/var/backup/home.MMDDYYYY.tar`.
        mv /var/backup/home.tar /var/backup/home.01012020.tar

        # Creates an archive of `/home`and saves it to `/var/backup/home.tar`.
        tar cvf /var/backup/system.tar /home 	

        # List all files in `/var/backup`, including file sizes, and save the output to `/var/backup/file_report.txt`.
        ls -lh /var/backup > /var/backup/file_report.txt

        # Print how much free memory your machine has left. Save this to a file called `/var/backup/disk_report.txt`.
        free -h > /var/backup/disk_report.txt


3. Create a script file called `update.sh` that does the following:

        #!/bin/bash

        # Ensure apt has all available updates
        apt update -y

        # Upgrade all installed packages
        apt upgrade -y

        # Install new packages, and uninstall any old packages that
        # must be removed to install them
        apt full-upgrade -y

        # Remove unused packages and their associated configuration files
        apt autoremove --purge -y

        # Bonus - Perform with a single line of code.
        apt update -y && apt upgrade -y && apt full-upgrade -y && apt-get autoremove --purge -y


#### Bonus

6. Create a file called `cleanup.sh` that does the following:
 
        #!/bin/bash

        # Clean up temp directories
        rm -rf /tmp/*
        rm -rf /var/tmp/*	

        # Clear apt cache
        apt clean -y

        # Clear thumbnail cache for sysadmin, instructor, and student
        rm -rf /home/sysadmin/.cache/thumbnails
        rm -rf /home/instructor/.cache/thumbnails
        rm -rf /home/student/.cache/thumbnails
        rm -rf /root/.cache/thumbnails


