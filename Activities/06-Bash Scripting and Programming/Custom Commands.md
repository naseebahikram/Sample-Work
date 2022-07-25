## Custom Commands

- In the previous activity, you created your first bash script. It contained a series of commands that should save you time during your system audits.

- In this activity, you will continue to make this script more complex by adding a few commands from the first exercise.

- As a bonus, you will save this script to a `scripts` directory and add that directory to your `$PATH` so you can call your script directly on the command line, from any directory.

Completing this activity will require the following:

- Ensure your script from the last activity runs as expected.

- Add the new commands listed in the instructions to your script.

- Save your script in a `~/scripts` directory.

- Add your `~/scripts` directory to your `$PATH`.

- Run your script to verify it produces the correct output.

#### Instructions

Complete the following inside your script.

- Add the command for creating a `~/research` directory to your script.
    - `mkdir ~/research 2> /dev/null`

- Add the command for finding `777` files to your script.
    - `echo -e "\n777 Files:" >> ~/research/sys_info.txt`

    - `find / -type f -perm 777 >> ~/research/sys_info.txt`
- Add the command for finding the Top 10 processes to your script.
    - `echo -e "\nTop 10 Processes" >> ~/research/sys_info.txt`
    - `ps aux -m | awk {'print $1, $2, $3, $4, $11'} | head >> ~/research/sys_info.txt`
- Modify each command of the script so that it writes all output to a file called `~/research/sys_info.txt`.
    - Add `>> ~/research/sys_info.txt` to each line of your script.

#### Bonus

Complete the following in your command line environment:

- Manually create a `~/scripts` directory and save your script there. (This should not be part of your script).
    - `mkdir ~/scripts && cp sys_info.sh ~/scripts`
- Add your `~/scripts` directory to your `$PATH`.
    - `echo "export PATH=$PATH:~/scripts" >> ~/.bashrc`
- Reload your bashrc file.
    -  `source ~/.bashrc`
- Run your script.
    -  `sys_info.sh`
- Open `~/research/sys_info.txt` and verify it has the desired output.
    - Run `less ~/research/sys_info.txt`
