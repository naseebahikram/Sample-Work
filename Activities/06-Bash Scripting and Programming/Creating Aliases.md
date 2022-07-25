## Creating Aliases

In the previous activity, you created longer commands by combining commands together to save time. Now, we will take things a step further and create some aliases for these commands along with some other commands that will save you more time when working at the command line.

- In this activity, you will create several aliases and save them to your `~/.bashrc` file so they will always be available.

- When completing this activity and creating aliases, consider the following:

    - Start by ensuring that each part of your command works correctly.
    - Ensure that the entire command works before creating the alias.
    - Use  `nano` to edit `~/.bashrc`, or use `echo` to echo your new alias into the `~/.bashrc` file.

**Remember**: if you get an error, check the file. Sometimes errors don't mean something is broken—they may just be informative messages that explain why a certain file was not included.

### Instructions

Create aliases in your `~/.bashrc` file for the following commands:


- `ls -a`
        - `echo "alias lsa='ls -a'" >> ~/.bashrc`

- `cd ~/Documents`
        - `echo "alias docs='cd ~/Documents'" >> ~/.bashrc`

- `cd ~/Downloads`
        - `echo "alias dwn='cd ~/Downloads'" >> ~/.bashrc`

- `cd /etc`
        - `echo "alias etc='cd /etc'" >> ~/.bashrc`


#### Bonus Aliases
- `nano ~/.bashrc`
    - `echo "alias rc='nano ~/.bashrc'" >> ~/.bashrc`

- `mkdir ~/research && cp /var/logs/* /etc/passwd /etc/shadow /etc/hosts ~/research`
    - `echo "alias logs='mkdir ~/research && cp /var/logs/* /etc/passwd /etc/shadow /etc/hosts ~/research'" >> ~/.bashrc`
