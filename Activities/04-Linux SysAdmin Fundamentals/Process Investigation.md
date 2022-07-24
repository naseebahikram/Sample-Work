## Process Investigation

- In the last activity, we completed a basic audit of the system and found some malicious script files and a user that was not supposed to be on the system. Now we will investigate all the processes running on the system to check if there are any obvious processes that should not be running.

- Your senior administrator has asked that you record snapshots of processes, as well as review the processes in real time for anything suspicious.

- You must review the processes that are running on the system to make sure nothing is amiss. If it is, you will want to `kill` that process and add what you found to your report.

### Instructions

Log into the lab environment with the following credentials: 
- Username: `sysadmin` 
- Password: `cybersecurity`

To get started with your activity, run the following command in your terminal: 

- `sudo bash /home/instructor/Documents/setup_scripts/instructor/processes.sh </dev/null &>/dev/null`

After which, you'll be able to use your terminal like usual.

Please read the following instructions and complete the steps.

1. During the last activity, you found a script file in a strange location on the system. Review the contents of this script file to get an idea of what commands you might be searching for.

    - List all the running processes in real time.
        - `top`

    - Review the help menu for this command and get a few ideas of what you want to investigate.
        - `man top`
    - Highlight the column that you are sorting by.
        - You can enable column highlighting and sorting by pressing the `x` key. By default, the `%CPU` column is highlighted and sorted by highest `CPU` usage.
2. To get an idea of how the system is currently running, answer these questions:

   - How many tasks have been started on the host?
        - `250`
   - How many of these are sleeping?
        - `0`
   - Which process uses the most memory?
        - `gnome-shell`

![2](images/2.png)

3. Search all running processes for a specific user.

    - Review all the processes started by the `root` or `sysadmin` user.
        - `u` followed by the name of the user
    - Sort by other users on the system that may be of interest.
        - `stress-ng` processes

![3](images/3.png)

**Bonus**     

4. Next, take a static "snapshot" of all currently running processes, and save it to a file in your home directory with the name `currently_running_processes`.

    - Use the flag to list all processes that have a TTY terminal.
        - `ps aux >> ~/currently_running_processes`
    - In the short list of output, do you notice any processes that seem suspicious?
        - `stress0ng --matrix 0 --times`. These commands intentionally stress the system and consume resources which could result in a Denial of Service from the server.

![4](images/4.png)

5. Identify the ID of any suspicious process. Stop that process with the `kill` command.
    - Run `kill <PID number>` or `kill 4714 4715`.

6.  `Kill` all processes launched by the user who started the command you just stopped. 
    - `sudo killall -u jack`
