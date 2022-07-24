## Using awk   
  
- You continue in your role as security analyst at Wonka Corp.

- Your manager still needs your help finding information on the cybercriminal attempting to log into several administrative websites owned by Wonka.

- You are now tasked with isolating several fields from the log file to determine the primary username being used to log in.

### Instructions

Using only the command line, complete the following tasks from within the `/03-student/day3/learning_awk` folder in your Ubuntu VM:
    - `cd /03-student/day3/awk_activity`

  1. Move `Update1_Combined_Access_logs.txt` into the directory `/03-student/day3/learning_awk`.
   - `mv /03-student/day3/learning_sed/Update1_Combined_Access_logs.txt .`

  1. Use the `awk` command to isolate the time and username fields out from this file.
    - `cat Update1_Combined_Access_logs.txt`
  - `awk '{print $4, $6}' Update1_Combined_Access_logs.txt`

  1. Use redirection to place these results into a new file called `Update2_Combined_Access_logs.txt`. 
  - `awk '{print $4, $6}' Update1_Combined_Access_logs.txt > Update2_Combined_Access_logs.txt`

