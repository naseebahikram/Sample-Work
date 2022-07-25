## Compound Commands

In the previous Linux classes you learned a lot of different commands, which you typically execute one at a time. Now we can start combining commands together to save us time when working on the command line.

In this activity, you are working on auditing a new system and would like to simplify your job with automation. You will begin by combining several commands together to make fewer overall commands.

This exercise will give you an opportunity to explore creating some useful commands that combine several steps from the system audit we did on Linux Day 1.


Consider the following when completing this activity: 

  - Start by making sure that each command works on its own.

  - Add just one command at a time, ensuring that the entire line runs as you expect before adding more commands.

  - If you are unable to complete the command even with `sudo`, become the `root` user and run it again. 


Reminders of common programs you can chain together:

- `head` prints only the first 10 lines of output.
- `tail` prints only the last 10 lines of output.
- `sort` sorts the output alphabetically.
- `sed`  searches and replaces parts of the output.
- `awk`  displays only specified parts of the output.

#### Instructions

1. Create a research directory and copy all system logs along with the `shadow`, `passwd`, and `hosts` files in one long command.

- Run `mkdir ~/research && cp -r /var/log/* /etc/passwd /etc/shadow /etc/hosts ~/research`


2. Create a list of all executable files in the home folder and save it to a text file in the research folder with one long command.
- Run `sudo find /home -type f -perm 777 > ~/research/exec_lst.txt`

3. Create a list of the 10 most active processes. The list should only contain the `USER`, `PID`, `%CPU`, `%MEM` and `COMMAND`. Save this list to a text file in your research directory with one long command.
- Run: `ps aux --sort -%mem | awk {'print $1, $2, $3, $4, $11'} | head > ~/research/top_processes.txt`

#### Bonus

- Create a list of home folders along with user info from the `passwd` file. Only add the user info to your list if the `UID` is greater than 1000.

   - Run: `ls /home > ~/research/users.txt && cat /etc/passwd | awk -F ":" '{if ($3 >= 1000) print $0}' >> ~/research/users.txt`

