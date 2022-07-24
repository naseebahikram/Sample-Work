## Service Users

- In the previous activity, we stopped and removed a few old services from the system.

- In this activity, you will continue auditing the same server for your senior administrator.

- The senior administrator would like you to remove any old service users from the system and create a new user that will be dedicated to running the Tripwire program.

- To complete this activity, you will use the `adduser` and `deluser` commands with the correct flags to clean up the system and create this new Tripwire user. 

    - Tripwire can only be run as `root`, so you will also need to add a line to the `sudoers` file to allow this.

### Instructions

1. To clean up our system and to prevent any unwanted abuse of remnant service users, remove the following service users associated with the services that you removed in the previous activity:

    - Service users for the `vsftpd` service
    
        - We can quickly find these users with `grep "ftp\|dove" /etc/passwd`

        - To remove the service users, run `sudo deluser --remove-all-files <username>` for each user. 

            - For example, `sudo deluser --remove-all-files dovecot`


2. Create a `tripwire` user that will be dedicated to running Tripwire.

    - Run `sudo adduser --system --no-create-home tripwire`

    - Run `id tripwire` and verify that the `UID` is less than 1000.

    - Run `ls /home` to verify there is no `tripwire` home folder.

    Remember, we can observe password entries in the `/etc/shadow` file.

     - Run `sudo tail /etc/shadow`

    The `*` in the password field for the Tripwire user means the user is locked without a password.

     - Run `sudo tail /etc/passwd`

    Note that `usr/sbin/nologin` is at the end of the Tripwire line. 

3. Add a line to the `sudoers` file to allow this user to run only `tripwire` using `sudo` privileges.
    - Run `sudo visudo`

    - Add `tripwire ALL= NOPASSWD: /usr/sbin/tripwire` to the user section of the file and save it.
4. Change the permission of the `tripwire` program to only allow the `owner` to execute.

    - Run `which tripwire` to locate the `tripwire` package.

    - Run `sudo chmod 700 /usr/sbin/tripwire`

    - Run `ls -l /usr/sbin/tripwire` to verify.
