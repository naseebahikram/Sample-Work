## Variables and If Statments

In the previous class, you created your first bash script, edited $PATH variables to create custom commands and added aliases to your `~/.bashrc` file.

Now, we will add variables and conditional `if` statements to our scripts.

`If` statements improve our scripts by allowing us to:

- Check if a file or directory exists before we create it.
- Check what user has run the script.
- And more...

To complete this activity, you will create variables and if statements that satisfy given requirements and use them in your script.

### Instructions

Consult this list of bash conditional operators while completing the activity:

- `=` : Checks if two items are `equal`.

- `!=` : Checks if two items are `not equal`.

- `-gt` : Checks if an integer is `greater than` another.

- `-lt` : Checks if an integer `less than` another.

- `-d /path_to/directory` : Checks for existence of a directory.

- `&&` : Both conditions have to be true to run.

- `||` : One condition has to be true to run.


#### Using Variables

1. Create a variable to hold the path of your output file.

    - Replace the output file path for each command with your variable.
        - `output=$HOME/research/sys_info.txt`
#### Using If Statements

1. Create an `if` statement that checks for the existence of the `~/research` directory.

    - If the directory exists, do nothing. If the directory does not exist, create it.

    - Remove the line in your script that creates this directory.


        - First, remove:

        `mkdir ~/research 2> /dev/null`


        - Then, replace it with an if statement that checks for the existence of the `~/research` directory.

        ```bash
        if [ ! -d $HOME/research ]
        then
        mkdir $HOME/research
        fi
        ```

#### Bonus Variables
If you have already completed the exercises above, see if you can complete the following:

1. Create a variable to hold the output of the command: `ip addr | grep inet | tail -2 | head -1`.

    - Replace this command in your script with your new variable.
        - `ip=$(ip addr | head -9 | tail -1)`.

2. Create a variable to hold the output of the command: `find /home -type f -perm 777`.

    - Replace this command in your script with your new variable.

        - `execs=$(find /home -type f -perm 777)`

#### Bonus If Statement

1. Protect the script from root! Create an `if` statement that checks if the script was run using `sudo`.

    - If it was run with `sudo`, exit the script with a message that tells the user not to run the script using `sudo`.

```bash
if [ $UID -ne 0 ]
then
  echo "Please run this script with sudo."
  exit
fi
```