# Homework: 4  The Linux Filesystem

Watch the video [“Linux Filesystem Explained”](https://www.youtube.com/watch?v=HbgzrKJvDRw) and read the presentation [“How to navigate the filesystem”](http://bit.ly/3t30rMQ) then answer the questions below.

1. **Explain the difference between absolute path and relative path:**

    Absolute path contains the full path from the root directory to the file like `~/home/user/Downloads/Movies/LOTR.mp4`

    With this path, a user can access the file from any directory he/she is in.

    Relative path contains only the child directories paths to the file like for example a user is in Downloads folder and he wants to access the LOTR.mp4 which is `Movies` folder. Now he/she can type a relative path as opposed to full path like `Movies/LOTR.mp4` and can access the file. Now this way, the user cannot access the file from any other directory, since whatever directory he/she is in, it may not contain `Movies` folder.

2. **Why Linux uses / instead of \ for its directory paths?**

    Linux is  Unix-like operating system, and in Unix forward slash `/` is used to navigate in directories. So that is why, linux uses `/`.


3. **In Windows, these files are all the same: File FILE file and FiLE. But in Linux this is not the case, Why?**

    Linux is  Unix-like operating system, so as unix files are case sesitives, in linux files are also case sesitives. In UNIX, all the system has to do is sort on the ASCII values of the letters of the filenames. This allows people to have every possible command and workflow to have a distinct, deterministic result. Windows is made for general purpose computing in mind at first and should be easier for a normal user to interact with the OS, so its file names are non case sesitive.

4. **What is the Filesystem Hierarchy Standard (FHS) and who maintains it?**

    FHS is a standard linux distros follows which has instructions/rules on how a filesystem on linux should be, what are its paths, names, directories etc. The FHS is maintained by The Linux Foundation. 


5. **Explain what type of files are stored in the following directories:**

Directory | What is it used for?
--------- | --------------------
/bin    | used for running scripts and commands especially for sys admins
/dev    | used for accessing drives like CD-ROM, USB etc
/etc    | contains configuration files which are used by various programs
/home   | used to store personal files
/lib    | libraries are stored used by programs and binaries /bin and /sbin     
/opt    | used by vendors to include add-on applications
/tmp    | used by system to store temp files created and maintained druing session and deleted once system reboots
/var    | used by programs and system to store files which could grow in size like log files etc
/proc   | used by ssytem to store information of system hardware, software and running processes
/usr    | used to install non essential applications

6. **How does a period at the beginning of a file name means (example .bashrc)?**

    A period at the start of a filename is used to indicate configuration and/or hidden files

7. **Which command would you use to list all the files inside the /usr/share/ directory?**

    The `ls` command list all the files inside te current directory.


8. **If you are working in the /usr/share/icons directory and want to move to your home directory, which command would you use?**

    The `cd ~` is used to move to your home directory.

9. **Explain what these commands do:**

`cd .config/.htop; cd ../; ls -lX`

`cd .config/.htop` goes into the hidden folder named config and executes a hidden file named htop

`cd ../` goes one directory back

`ls -lX` shows the names of all the files in the current directory alphabetically ordered in ascending

10. **John has a lot of files in the directory /var/www/html/webapp. He wants to long list all the files, including hidden files, by modification time (newest first), and with human-readable file sizes. Which command should he use conjuring that his current working directory is:** 
    
`/home/john/.git/`

`ls -ljgGs ~/var/www/html/webapp`