## Log Size Management

In this activity, you are a junior administrator at Rezifp Pharma Inc. The company maintains a large database of patient data associated with patients, doctors, and their treatments. These files are maintained on a local server.

The primary benefits of log rotation are preserving log entries and keeping log file sizes manageable. When a log file is rotated, the preserved log file can be compressed to save space.

You will create a log rotation scheme that keeps four weeks' worth of logs with a daily rotation that includes a maximum file size of 1 GB.

### Instructions


In your Ubuntu VM, launch a terminal. 

1. Verify you have the most up-to-date version of logrotate installed. 
    - Run `sudo apt install logrotate`
2. Configure the following default parameters for logrotate by editing `/etc/logrotate.conf`: 

   - Run `sudo nano /etc/logrotate.conf` and add the following update: 

        -	Implement a rotation scheme to keep four weeks of backlogs.

            ```bash
            # Keep 4 weeks of backlogs
            rotate 4
            ```

        -	Create new empty log file after rotating old ones.

            ```bash
            # Create new (empty) log file after rotating old ones
            create
            ```

        -	Do not rotate empty logs.

            ```bash
            # Do not rotate empty logs
            notifempty
            ```

        -	Compress log files.

            ```bash
            # Compress log files
            compress
            ```

3. List the contents of `logrotate.d` to see what configuration files are present.
     - Run  `ls -lat /etc/logrotate.d`
4. In `/etc/logrotate.d`, add configurations for the following directories:

     `/var/log/auth.log` parameters: `180 days of backlog`, `rotate daily`, `Don't rotate empty logs`, `Compress the file`, `Delay the compression`.

    - Run `nano auth` to create a new file. 
    
    - Add the following contents: 

        ```bash
        /var/log/auth.log {
            rotate 180
            daily
            notifempty
            compress
            delaycompress
            endscript
        }
        ```
     - Save and exit the file. 
    
    `/var/log/cron.log` parameters: `60 days of backlog`, `rotate daily`, `Don't rotate empty logs`, `Compress the file`, `Delay the compression`.
    
     - Run `nano cron` to create a new file. 
    
     - Add the following contents: 


        ```bash
        /var/log/cron.log {
            rotate 60
            daily
            notifempty
            compress
            delaycompress
            endscript
        }
        ```
     - Save and exit the file. 

    `/var/log/boot.log` parameters: `30 days of backlog`, `rotate daily`, `Don't rotate empty logs`, `Compress the file`, `Delay the compression`.

     - Run `nano boot` to create a new file. 
    
     - Add the following contents: 

        ```bash
        /var/log/boot.log {
            rotate 30
            daily
            notifempty
            compress
            delaycompress
            endscript
        }
        ```
     - Save and exit the file. 


#### Bonus

5. Test the rotation by forcing logrotate to rotate the logs by verifying the dates.

    - Make sure that the proper lines are un-commented in the `etc/logrotate.conf` file. 

   - Run `sudo logrotate -vf /etc/logrotate.conf`. If you see `old log` in the output, run the command again until you see `rotating pattern` in the output.
