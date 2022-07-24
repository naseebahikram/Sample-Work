## Gathering Evidence
 
- In this activity you will continue your role as a security analyst at Wonka Corp. 

- Wonka Corp believes they have enough evidence to send to the authorities to charge Slugworth with a cyber crime. 

- Your task is to gather several points of evidence from your file systems that can be provided to the authorities to prove Slugworth is stealing data.

### Instructions

Using only the command line, continue to complete the following tasks in the `/03-student/day2/Gathering_Evidence` folder in your Ubuntu VM:
   - `cd /03-student/day2/Gathering_Evidence/`

1.  In the `Gathering_Evidence` folder, make a directory called `Slugworth_evidence`.
  - `mkdir Slugworth_evidence`

2. The `email` directory contains an archive of emails from the employees.
 Place into a  new file called `slugworth_email_evidence` the following data:
    - List of emails referencing Slugworth.
    - Number of emails referencing Slugworth.
  
    **Hint:** Use the pipe and redirection command to append the additional data to this file.
   
- `cd email`
- `grep -il slugworth * > slugworth_email_evidence`
- `grep -il slugworth * | wc -l >> slugworth_email_evidence`

 3. The `web_logs` directory contains an archive of web log access by date for PeanutButtery.net. The IP of Slugworth, which is a numerical number that identifies an address on the network, is `13.16.23.234`.
    - Place into a  new file called `slugworth_web_evidence` the following data:
    
      - Which web log file contains the IP address of Slugworth.
      - The number of times Slugworth's IP is found in this file.

   - `cd web_logs`
   - `grep -il 13.16.23.234 * > slugworth_web_evidence`
  - `grep -i 13.16.23.234 * | wc -l >> slugworth_web_evidence`

4. Move the two new evidence files into the directory `Slugworth_evidence`.
    - `cd ../../`
    - ` mv ./Gathering_Evidence/email/slugworth_email_evidence ./Gathering_Evidence/Slugworth_evidence/`
    - `mv ./Gathering_Evidence/web_logs/slugworth_web_evidence ./Gathering_Evidence/Slugworth_evidence/`  
5.  Combine them both into a single file into a file called `Slugworth_evidence_for_authorities`.
  - `cd Gathering_Evidence/Slugworth_evidence/`  
  - `cat slugworth_email_evidence slugworth_web_evidence > Slugworth_evidence_for_authorities`
