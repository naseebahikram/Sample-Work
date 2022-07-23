## Take Five and Practice the Command Line

- You are playing the role of a security analyst at Wonka Corp. 

- Wonka Corp believes one of their employees might be selling secret recipes to Slugworth Corp.

- You have been tasked with creating evidence files for email, logs, and web access.  

- These files are currently empty, but will be used later to organize your investigation notes on the rogue employee.

### Instructions

Using only the command line, complete the following tasks from within the `/03-student/day1/take_5/` folder in your Ubuntu VM:
    - `cd /03-student/day1/`
    - `cd take_5`

1. Create a folder called `Internal_Investigation_Employee_A`.

    - `mkdir Internal_Investigation_Employee_A`

2. Navigate into the `Internal_Investigation_Employee_A` folder.

    - `cd Internal_Investigation_Employee_A`

3. From within the `Internal_Investigation_Employee_A` folder, print the working directory to confirm you are in the correct place.

    - `pwd`

4. Create three files inside the `Internal_Investigation_Employee_A` folder:
    * `email_evidence`
    * `log_evidence`
    * `web_evidence`

        - `touch email_evidence log_evidence web_evidence`

5. Delete the file called `web_evidence` as you realized Wonka has no web logs captured.

    - `rm  web_evidence`

6. Display (list) all the files created.

    - `ls`

7. Clear the terminal window.

    - `clear`
