# Theory
- **What is Linux OS? What is the difference between Linux and Unix?**
  - Linux is an open source multi-tasking, multi-user operating system. It was initially developed by Linus Torvalds in 1991. 
  - Linux OS is widely used in desktops, mobiles, mainframes etc.
  - Linux is a family of open-source Unix-like operating systems based on the Linux kernel.
  - ![image](https://user-images.githubusercontent.com/68856476/162609531-d57be9c5-ee3c-4d92-aa3c-3d9cf7ad07ab.png)
---------------------------------------------------------------
- **What are the basic components of Linux?**
- The kernel
  - The kernel is the heart of any unix os.
  - This kernel is relatively a small piece of code written in ‘c’ that is embedded on the hardware.
  - Every unix system has a kernel that gets automatically loaded on to the memory as soon as system is boosted.
  - The kernel is the only component that can communicate with all hardware directly.
  - Kernel manages all the system resources like memory and i/o devices, allocated time between users and processes in the case of multi-user environment, decides process priorities, manages inter process communication and performs many other such tasks.
- The shell
  - Every unix system has atleast one shell.
  - A shell is a program that sites on kernel and acts as an agent or interface between the users and the kernel and hence the hardware.
  - A shell is a command interpreter or processor at which the user can type in any unix command.
- The file system.
  - A file system is another major component of a unix system.
  - Unix treats every thing including hardware devices as a file.
  - All the files in a unix system are organized in an inverted tree-like hierarchial structure .
---------------------------------------------------------------
- **What do you mean by Linux? Explain its features.** 
- Linux is a family of open-source Unix-like operating systems based on the Linux kernel
- Following are some of the important features of Linux Operating System.
- Portable 
  - Portability means software can works on different types of hardware in same way. Linux kernel and application programs supports their installation on any kind of hardware platform.
- Open Source
  - Linux source code is freely available and it is community based development project. Multiple teams work in collaboration to enhance the capability of Linux operating system and it is continuously evolving.
- Multi-User
  - Linux is a multiuser system means multiple users can access system resources like memory/ ram/ application programs at same time.
- Multiprogramming 
  - Linux is a multiprogramming system means multiple applications can run at same time.
- Hierarchical File System 
  - Linux provides a standard file structure in which system files/ user files are arranged.
- Shell 
  - Linux provides a special interpreter program which can be used to execute commands of the operating system. It can be used to do various types of operations, call application programs. etc.
- Security 
  - Linux provides user security using authentication features like password protection/ controlled access to specific files/ encryption of data.
---------------------------------------------------------------
- **Which are the Shells used in Linux?**
- SHELL is a program which provides the interface between the user and an operating system. 
- When the user logs in OS starts a shell for user. Kernel controls all essential computer operations, and provides the restriction to hardware access, coordinates all executing utilities, and manages Resources between process. 
- Using kernel only user can access utilities provided by operating system.
- The C Shell : Denoted as csh
  - It incorporated features such as aliases and command history. It includes helpful programming features like built-in arithmetic and C-like expression syntax.
- The Bourne Shell : Denoted as sh 
  - It is the original UNIX shell. It is faster and more preferred. It lacks features for interactive use like the ability to recall previous commands. It also lacks built-in arithmetic and logical expression handling. It is default shell for Solaris OS.
- The Korn Shell : Denoted as ksh 
  - its superset of the Bourne shell.So it supports everything in the Bourne shell.It has interactive features. It includes features like built-in arithmetic and C-like arrays, functions, and string-manipulation facilities.It is faster than C shell. It is compatible with script written for C shell.
- GNU Bourne-Again Shell : Denoted as bash 
  - It is compatible to the Bourne shell. It includes features from Korn and Bourne shell.
---------------------------------------------------------------
- **Explain how to change file permissions in Linux with suitable examples.**
- We can use the ‘chmod’ command which stands for ‘change mode’. 
- Using the command, we can set permissions (read, write, execute) on a file/directory for the owner, group and the world.
- ```chmod permissions filename```
---------------------------------------------------------------
- **State the advantage of using hierarchical method of file system organisation.**
- if binaries are all in one location, it's easy to protect them by limiting write-access with permissions
- if configuration information is in a separate location, it's easy to change or backup configuration as needed, and apply appropriate permissions
- program assets such as documentation may need more accessibility to users and different permissions as well.
- if libraries are in their own central location, any program can access them and when they are updated any program using them will use the updated version.
---------------------------------------------------------------
- **Explain file permission in Linux.**
- Every file, directory, and other system objects in Linux are assigned an owner and a group. 
- This is the most basic, yet essential, part of system security that protects users from each other. 
- Owners, users belonging to a group, and all others may be granted different types of access to read from, write to, or execute files. 
- This is generally referred to as file permissions in Linux.To set permissions and manage ownership, we will use the following commands:
  - chmod : change file permissions
  - chown : change file owner
  - chgrp : change group ownership
---------------------------------------------------------------
- **What are the features of sudo?**
- Sudo (superuser do) is a utility for UNIX- and Linux-based systems that provides an efficient way to give specific users permission to use specific system commands at the root (most powerful) level of the system. 
- Sudo also logs all commands and arguments. 
- Using sudo, a system administrator can:
  - Give some users (or groups of users) the ability to run some (or all) commands at the root level of system operation
  - Control which commands a user can use on each host
  - See clearly from a log which users used which commands
  - Using timestamp files, control the amount of time a user has to enter commands after they have entered their password and been granted appropriate privileges
---------------------------------------------------------------
- **Which are the Linux Directory Commands?**
- pwd : This command displays the present working directory where you are currently in.
- ls : This command will list the content of a directory.
- ls -la : This command will list all the content of a directory including the hidden files and directories.
- mkdir <path> : This command will create a new directory, provided it doesn't exists.
- mkdir -p  <path> : This command will create nested directories.
- rmdir <path> : This command will remove/delete an existing directory, provided it is empty.
- cd <path> : This command is used to change directory.
- cd .. : This command will take us one level up the directory tree.
- touch <filename> : This command will creates a new file.
- rm <filename> : This command will delete a file.
- rm -f <filename> : This command forcefully deletes a file.
- rm -r <directory> : This command deletes a directory recursively along with its content.
- rm -rf <directory> : This command forcefully and recursively deletes a directory along with its content.
- cp <file1> <file2> : This command copies the content of file file1 into file file2.
- cp -r <dir1> <dir2> : This command copies the content of directory dir1 into directory dir2.
- mv <path1> <path2> : rename/Move files and directories
- cat <file> : This will print the content of a file.
- head <file> : This command will print the first 10 lines of a file.
- tail <file> : This command will print the last 10 lines of a file.
- tail -f <file> : This will print the last 10 lines of a file and will keep printing new lines as they get appended to the file.
---------------------------------------------------------------
- **Which are the different modes of vi editor?**
- Command Mode: 
  - When vi starts up, it is in Command Mode. This mode is where vi interprets any characters we type as commands and thus does not display them in the window. This mode allows us to move through a file, and to delete, copy, or paste a piece of text.To enter into Command Mode from any other mode, it requires pressing the [Esc] key. If we press [Esc] when we are already in Command Mode, then vi will beep or flash the screen.
- Insert mode: 
  - This mode enables you to insert text into the file. Everything that’s typed in this mode is interpreted as input and finally, it is put in the file. The vi always starts in command mode. To enter text, you must be in insert mode. To come in insert mode you simply type i. To get out of insert mode, press the Esc key, which will put you back into command mode.
- Last Line Mode(Escape Mode): 
  - Line Mode is invoked by typing a colon [:], while vi is in Command Mode. The cursor will jump to the last line of the screen and vi will wait for a command. This mode enables you to perform tasks such as saving files, executing commands.

---------------------------------------------------------------
---------------------------------------------------------------  
  
# Commands
### man :
  - man command in Linux is used to display the user manual of any command that we can run on the terminal. 
  - ```$ man mkdir ```
### who :
  - The Linux "who" command lets you display the users currently logged in to your UNIX or Linux operating system.
  - ```$ who```
### whoami :
  - whoami is an basic Unix/Linux command used to find username associated with current effective user id.
  - ```$ whoami```
### vim : 
  -  VI editor is the most popular and classic text editor in the Linux family.
  - ```$ vim <file>```
  - i > insert-mode , add text , escape , :wq > save & quite
### wc :
  - It is used to find out number of lines, word count, byte and characters count in the files specified in the file arguments.
  - ```$ wc <file>```
### rm :
  -  This command will delete a file.
  - ```$ rm <filename>```
### mkdir : 
  - This command will create a new directory, provided it doesn't exists.
  - ```$ mkdir <path>```
### rmdir :
  - This command will remove/delete an existing directory, provided it is empty.
  - ```$ rmdir <path>```
### touch :
  -  This command will creates a new file.
  - ```$ touch <file>```
### mesg :
  - mesg command allows you control write access to your terminal by other users.
  - ```$ mesg [n|y]``` : update state
  - ```$ mesg``` : current state
### write :
  - write command in Linux is used to send a message to another user.
  - ```$ write <user>```
### grep :
  - The grep filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern. 
  - ```$ grep [options] pattern [files]```
  - -i : ignore case-sensitive
  - -c : count
### uname
  - uname command is used to display basic information about the operating system and hardware.
  - ```$ uname -u``` : kernel name
  - ```$ uname -r``` : kernel release
### tty 
  -  print the file name of the terminal connected to standard input
  - ```$ tty```
### passwd
  - The passwd command changes passwords for user accounts.
  - ```$ passwd -S garvit9000```
  - ```$ man passwd``` : manual
### date
  - return current date of system
  -```$ date```
### cal
  - print calendar of current month
  - ```$ cal```
### bc 
  - command line calculator
  - ```echo "12+5" | bc```
### clear
  - clear terminal
  - ```$ clear```
### ls
  - returns all files & directory in current working directory
  - ```$ ls```
### pwd
  - return present working directory
  - ```$ pwd```
### cd
  - change directory
  -```$ cd <path>```
### cat
  - print all file content
  - ```$ cat <file>```
### more
  - more command is used to view the text files in the command prompt, displaying one screen at a time in case the file is large 
  - ```$ more <file>```
### cp
  - This command copies the content of file file1 into file file2.
  - ```$ cp <file1> <file2>``` 
### mv
  - rename/Move files and directories
  - ```$ mv <path1> <path2>``` 
### chmod
  - the chmod command is used to change the access mode of a file.
  - ```$ chmod [reference][operator][mode] file```
  - reference : u(user),g(group),o(other),a(all)
  - operator :
    - (+)Adds the specified modes to the specified classes
    - (-)Removes the specified modes from the specified classes
    - (=)The modes specified are to be made the exact modes for the specified classes
  - mode : r(read),w(write),x(execute)
### tail
  - This command will print the last 10 lines of a file.
  - ```$ tail <file>```
### head
  - This command will print the first 10 lines of a file.
  - ```$ head <file>```
### chown
  - chown command is used to change the file Owner or group
  - ```$ chown owner_name file_name```
### chgrp
  - chgrp command in Linux is used to change the group ownership of a file or directory
  - ```$ sudo addgroup geeksforgeeks```
  - ```$ sudo chgrp geeksforgeeks abc.txt```
### ln
  - ln is a command-line utility for creating links between files. By default, the ln command creates hard links. To create a symbolic link, use the -s (--symbolic) option
  - ```$ ln -s source.txt link.txt```
### echo 
  - echo command in linux is used to display line of text/string that are passed as an argument .
  - ```$ echo [string]```
### ps
  - ps command is used to list the currently running processes and their PIDs 
  - ```$ ps```
### kill
  - command which is used to terminate processes manually
  - ```$ kill -l```To display all the available signals
  - ```$ kill <pid>```
-----------------------------------------------------------------------------------------
  
  
  
  
  
  
  
  
  
  
  
  
  
