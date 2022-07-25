## My First Bash Script

- In the previous activity you created several aliases and saved them to your `~/.bashrc` file. You may have noticed that creating long strings of commands can get a bit cumbersome when working on the command line.

- Now, we will put our commands into a script file. Reading, writing, and running Bash scripts are a staple of any good sysadmin.

- In this activity, you will create a script that completes several system audit steps automatically.

When completing this activity, consider the following:

- Start by ensuring each command will give you the expected output before adding it to your script.

- Some commands may not have been covered and require additional research.
- Add all the commands listed in the instructions to your script.
- Ensure the output of each command has a title like: `The Memory Info is:`
- Change the permissions on your script to make it executable.
- Run your script to verify it produces the correct output.

As a reminder, here are a few helpful environment and shell variables:

- `USER`
- `HOME`
- `SHELL`
- `PWD`
- `BASH`
- `HOSTNAME`
- `MACHTYPE`
- `UID`


### Instructions

Complete the following set-up:

- Create a new script file called `sys_info.sh`.
    - `touch sys_info.sh`

- Change the permissions on the file to make it executable.
    - `chmod +x sys_info.sh`

- Open the file with `nano`.
    - `nano sys_info.sh`

- Add a top `hashbang` line to make this a bash script.

    - `#!/bin/bash`

Your script should output the following data:

- A title 
    - `echo "A Quick System Audit Script"`

- The `uname` info for the machine.
-  `echo -e "Uname info: $(uname -a) \n"`'

- The machine's IP address. (Narrow this output down to one line.)
    -  `echo -e "IP Info: $(ip addr | head -9 | tail -1) \n"`

- The Hostname.
    - `echo "Hostname: $(hostname -s) "`

Run your script using `./` notation.

#### Bonus Script Ideas

If you complete the script above, try adding a few of these items:
The DNS info.

  - `echo "DNS Servers: "`

  - `cat /etc/resolv.conf`

    The `DNS` info is stored in the `/etc/resolv.conf` file. All we need to do is display the contents of this file using `cat`.

The Memory info.

  - `echo "Memory Info:"`

  - `free`

The CPU info.

  - `echo -e "\nCPU Info:"`

    -  `echo -e "\nCPU Info:"` gives us a title with a line break before it.


  - `lscpu | grep CPU`

    - `lscpu` gives us a ton of info about the computer's CPU.
    - Remember: `ls` has a number of extended commands to show hardware and other system info. 
    - `| grep` pipes that output into `grep` so we can parse just the info we want.
    - `CPU` is given to `grep` to display lines that only contain `CPU`.



The Disk usage.
- `echo -e "\nDisk Usage:"`
- `df -H | head -2`
    - `df` retrieves the disk information.
    - `-H` displays the info in `human readable` format. This means it will display bytes in `megabytes` an `gigabytes` instead of `bytes`.
    - `| head`: Again, we are piping the command into the `head` command to limit output.
    - `2` limits the output of `head` to 2 lines.


The currently logged on users.

- `echo -e "\nWho is logged in: \n $(who -a) \n"`

  - `echo -e "\n` initiates our `echo` command and creates a line break.
  - `Who is logged in: \n` will be printed as shown with another line break.
  - `$(who)` runs the `who` command before the `echo` command.
  - ` \n` provides another line break.

Run the script:
    - `./sys_info.sh`
