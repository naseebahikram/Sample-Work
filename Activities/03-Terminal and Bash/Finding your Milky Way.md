## Finding your Milky Way 
 
- You will continue in your role as security analyst at Wonka Corp, investigating the employee potentially selling secret recipes to Slugworth Corp.

- Your manager at Wonka Corp needs you to create an additional directory, as they believe there is a second employee working with Slugworth Corp.

- You also must copy and move several of the evidence files after creating this new directory.

### Instructions

Using only the command line, continue to complete the following tasks in the `/03-student/day1/take_5` folder in your Ubuntu VM:
    - `cd /03-student/day1/take_5`

1. Create an additional folder called `Internal_Investigation_Employee_B`.

    - `mkdir Internal_Investigation_Employee_B`

2. Using absolute paths, move the file `email_evidence` from `Internal_Investigation_Employee_A` to `Internal_Investigation_Employee_B` as you have been told there will not be email evidence for the first employee. 

    - `mv /03-student/day1/take_5/Internal_Investigation_Employee_A/email_evidence /03-student/day1/take_5/Internal_Investigation_Employee_B/`

3. Using absolute paths, copy the file `log_evidence` from `Internal_Investigation_Employee_A` to `Internal_Investigation_Employee_B`, as you have been told there will likely be log evidence from both employees.

    - `cp /03-student/day1/take_5/Internal_Investigation_Employee_A/log_evidence /03-student/day1/take_5/Internal_Investigation_Employee_B/`

4. Check your directories to confirm the files are all in the correct locations.

    - `cd /03-student/day1/take_5/Internal_Investigation_Employee_A/`
        - `ls`
    - `cd /03-student/day1/take_5/Internal_Investigation_Employee_B/`
        - `ls`