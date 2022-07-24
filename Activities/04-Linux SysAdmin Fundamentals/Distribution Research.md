## Distribution Research

- Recently, your organization experienced a number of breaches involving servers running outdated Linux distributions.

- In response, the IT Department has decided to upgrade the affected servers, and chose you as the **system administrator** in charge of deciding which distribution to install on each machine.

- In this exercise, you will research the most common distributions of Linux and answer the following questions. Then you will use what you learn to determine which distribution is most appropriate for each machine on the network.

Be sure to ask your instructors and classmates for help if you get stuck.


### A. Resources and Research
Use the following links to answer the questions below:

- [Debian Linux](https://www.debian.org/intro/about)
- [Ubuntu Linux](https://www.ubuntu.com/download)
- [Kali Linux](https://www.kali.org/about-us/)
- [RedHat](https://www.redhat.com/en/technologies)
- [Fedora](https://getfedora.org/)
- [CentOS](https://www.centos.org/about/)
- [SELinux](https://selinuxproject.org/page/Main_Page)
- [Mint Breach](https://www.techrepublic.com/article/why-the-linux-mint-hack-is-an-indicator-of-a-larger-problem/)

1. Which distribution is most flexible and best suited for day-to-day and administrative tasks?
    - Ubuntu

2. Which distribution is built specifically for penetration testers?
    - Kali

3. Which distributions would you use to set up a web or data server?
    - Really, you could use any of them, however, Ubuntu Server and Fedora Server both have easy-to-configure web services. If you wanted to do things more manually, you could use Debian or CentOS.

4. What is the most widely used Linux desktop environment?
    - Ubuntu
    
#### Bonus Questions

1. What is a "headless server"?
    - A command line-only server without a desktop environment.

    -  1a. Does Ubuntu make a headless server variant? What about Fedora? CentOS?
         - Yes, all three of them do.

2. What distribution is Ubuntu based on? What about Kali?
    - They are both based on Debian.

3. Which distribution is CentOS based on? What about Fedora?
    - They are both based on Red Hat.

4. What is SELinux? Which distributions implement SELinux by default?  
    - SELinux is a built-in file permissions security enhancement developed by the NSA. CentOS and Fedora have it implemented by default.

5. If you were deciding between versions of Ubuntu Server and wanted one  that will remain stable over time, which version would you choose?
    - You would choose the "Long Term Support" or _LTS_ version. The latest version is one that will have continual updates and changes. The _LTS_ version will remain stable and only changes about once a year.

6. What are some security implications of using free and open source software or forks of popular Linux distributions?
    - As demonstrated in the Mint OS article, _open source_ means that anyone can contribute. This makes it somewhat easy for an attacker with programing skills to attack. Because of this users, must be vigilant about where they get their software.