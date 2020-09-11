# Linux Interview Questions

### Content

- [I. Introduction to Linux](#I. Introduction to Linux)
- [II. Basics](#II. Basics)
  - [Shell Features](#Shell Features)
    - [x] [Q: How to choose your shell?](#Q: How to choose your shell?)
    - [x] [Q: What are basic shell commands?](#Q: What are basic shell commands?)
  - [Moving Around the Filesystem](#Moving Around the Filesystem)
    - [x] [Q: What are basic move around shell commands?](#Q: What are basic move around shell commands?)
    - [x] [Q: What is file matching metacharacters and brace expansion characters?](#Q: What is file matching metacharacters and brace expansion characters?)
    - [x] [Q: What is file redirection?](#Q: What is file redirection?)
    - [x] [Q: How to set file permissions and ownership?](#Q: How to set file permissions and ownership?)
    - [x] [Q: How to set default permissions by set umask?](#Q: How to set default permissions by set umask?)
    - [ ] [Q: What are file create, rename, remove, move commands?](#Q: What are file create, rename, remove, move commands?)
  - [Working with Text Files](#Working with Text Files)
    - [ ] [Q: What are common text file editors?](#Q: What are common text file editors?)
    - [ ] [Q: How to search files?](#Q: How to search files?)
    - [ ] [Q: How to search in files?](#Q: How to search in files?)
  - [Managing Processes](#Managing Processes)
    - [ ] [Q: How to display all processes?](#Q: How to display all processes?)
    - [ ] [Q: How to get the listen port of a process?](#Q: How to get the listen port of a process?)
    - [ ] [Q: How to kill processes?](#Q: How to kill processes?)
    - [ ] [Q: How to set process priority?](#Q: How to set process priority?) (NICE)
    - [ ] [Q: Running processes in foreground and background?](#Q: Running processes in foreground and background?)
- [III. Programming with Shell Script](#III. Programming with Shell Script)
  - [Shell Scripts Basics](#Shell Scripts Basics)
    - [ ] [Q: What is the first line in a shell script?](#Q: What is the first line in a shell script?)
  - [Variables](#Variables)
  - [Input and Output](#Input and Output)
  - [Control Flow](#Control Flow)
- [IV. Linux System Administrator](#IV. Linux System Administrator)
  - [Administration and Configuration](#Administration and Configuration)
  - [Managing Software](#Managing Software)
  - [Managing User Accounts](#Managing User Accounts)
    - [User Accounts](#User Accounts)
      - [ ] [Q: How to create a system user?](#Q: How to create a system user?)
      - [ ] [Q: How to get basic information of system users?](#Q: How to get basic information of system users?)
      - [ ] [Q: How to modify system users?](#Q: How to modify system users?)
      - [ ] [Q: How to delete system users?](#Q: How to delete system users?)
    - [User Groups](#User Groups)
      - [ ] [Q: How to get basic information of system groups?](#Q: How to get basic information of system groups?)
      - [ ] [Q: How to create a system group?](#Q: How to create a system group?)
      - [ ] [Q: How to modify system groups?](#Q: How to modify system groups?)
  - [Managing Disk and Filesystems](#Managing Disk and Filesystems)
- [V. Linux Server Administrator](#V. Linux Server Administrator)
  - [Networking](#Networking)
  - [Services](#Services)
    - [ ] [Q: What is initialization system (init)?](#Q: What is initialization system (init)?)
    - [ ] [Q: What is systemd?](#Q: What is systemd?)
    - [ ] [Q: How to write unit configuration files of systemd?](#Q: How to write unit configuration files of systemd?)
    - [ ] [Q: What are basic commands of systemd?](#Q: What are basic commands of systemd?)
  - [Configuring Servers](#Configuring Servers) (Web, FTP, NFS etc)
  - [Troubleshooting Linux](#Troubleshooting Linux)
- [VI. Linux Security](#VI. Linux Security)
  - [Firewall](#Firewall)
    - [ ] [Q: What is firewall?](#Q: What is firewall?)
    - [ ] [Q: How to use ufw to set firewall?](#Q: How to use ufw to set firewall?)
- [References](#References)

## Main

## I. Introduction to Linux

## II. Basics

## Shell Features

### Q: How to choose your shell?

Default shell is shown in 

```
$ grep <username> /etc/passwd
```

Running the following to show the root user default shell: 

```
grep root /etc/passwd
```

Output: 

```
root:x:0:0:root:/root:/bin/bash
```

Type shell name to entry other shell: `ksh`, `tcsh`, `csh`, `sh`, `dash`...

Type `$ exit` to return to bash shell.

### Q: What are basic shell commands?

Basic

```shell
# print current directory path
$ pwd
# print history commands
$ history
# print current datetime
$ date
# command reference manuals
$ man <command>
$ <command> --help

# list current directory files
$ ls
# go to a directory
$ cd <dir path>
# helps us move some data, usually text into a file
$ echo
$ cat
$ less
$ vi


# print userId, groupId
$ id
# print current system user name
$ whoami
# stands for "SuperUser Do". any command to be done with administrative or root privileges
$ sudo
```

Filesystem

```shell
# go to a directory
$ cd <dir path>
$ mkdir <dir>
$ rmdir <dir>
$ rm <file/dir>
$ touch <new_filename>
$ cp
$ mv
$ locate
$ find
$ tar
$ zip
$ unzip
$ chmod
$ chown
```

Text Files

```shell
# helps us move some data, usually text into a file
$ echo
# to display the contents of a file
$ cat
# view a text file
$ less
$ head
$ tail
$ diff

# text editor
$ nano
$ vi
# search text in files
$ grep
```

Administration

```shell
# to install packages
$ apt-get

# display processes
$ ps
$ top
# kill processes
$ kill

# to see the available disk space in each of the partitions in your system
$ df
# Display amount of free and used memory in the system
$ free
# estimate file space usage
$ du

# show system's host name
$ hostname
# show your IP address
$ hostname -I
# show your IP address
$ ifconfig
# to check your connection to a server
$ ping <domain>
```



## Moving Around the Filesystem

### Q: What are basic move around shell commands?

```shell
# go to a directory
$ cd <dir path>
$ mkdir <dir>
$ rmdir <dir>
$ rm <file/dir>
$ touch <new_filename>
$ cp
$ mv
$ locate
$ find
$ tar
$ zip
$ unzip
$ chmod
$ chown
```

### Q: What is file matching metacharacters and brace expansion characters?

 file matching metacharacters

```
*, ?, []
```

For example: 

```shell
# list files
$ ls g*t
$ ls test?.txt
$ ls [a-g]*
```

brace expansion characters

```
{}
```

For example: 

```shell
# create files
$ touch test{1,2,3,4,5}
```

### Q: What is file redirection?

- `<`: directs file content to the command. 

  ```
  $ less < bigfile
  ```

- `>`: directs standard output to a file. 

  ```
  $ ls > test.txt
  ```

- `2>`: directs standard error to file.

- `&>`: directs both standard output and error to file.

- `>>`: directs output append to a file.



### Q: How to set file permissions and ownership?

**Change permissions**

1. chmod with numbers

Permission numbers: 

- r=4, w=2, x=1

For example:

```shell
$ chmod 755 <filename>
# set entire directory permission
$ chmod -R 755 <dir_path> 
```

2. chmod with letters

Permission letters: 

- user(u), group(g), other(0), all users(a), read(r), write(w), execute(x)

For example:

```
$ chmod u+rw <filename>
```

**Changing file ownership**

```
$ chown <username> <filename>
$ chown <username>:<group_name> <filename>
$ chown -R <filename>
```



### Q: How to set default permissions by set umask?

Setting default file permission with umask:

Show umask value: 

```
$ umask
```

Output:

```
0022
```

You should ignore first number, the output value is 0002 as 022. The default **umask for the root user is 022** result into default directory permissions are 755 and default file permissions are 644.

The user mask contains the following octal values:

- The first digit sets permissions for the user
- The second sets permissions for group
- The third sets permissions for other, also referred to as “world”

To determine the umask value you want to set, subtract the value of the permissions you want from 666 (for a file) or 777 (for a directory). The remainder is the value to use with the umask command. For example, suppose you want to change the default mode for files to 644 (rw-r--r--). The difference between 666 and 644 is 022, which is the value you would use as an argument to the umask command.

1. The default **umask 002** used for normal user. With this mask default directory permissions are 775 and default file permissions are 664.
2. The default **umask for the root user is 022** result into default directory permissions are 755 and default file permissions are 644.

Permissions for umask Values

| umask Octal Value | File Permissions | Directory Permissions |
| ----------------- | ---------------- | --------------------- |
| `0`               | `rw-`            | `rwx`                 |
| `1`               | `rw-`            | `rw-`                 |
| `2`               | `r--`            | `r-x`                 |
| `3`               | `r--`            | `r--`                 |
| `4`               | `-w-`            | `-wx`                 |
| `5`               | `-w-`            | `-w-`                 |
| `6`               | `--x`            | `--x`                 |
| `7`               | `---` (none)     | `---` (none)          |

To temporarily change your umask value: `$ umask <umask_value>`. For example:

```
$ umask 002
```

To permanently change umask value, add a umask command to the `.bashrc` file in your home directory. The system umask defaults in their `/etc/profile file`, `~/.profile`.



### Q: What are file create, rename, remove, move commands?



## Working with Text Files

### Q: What are common text file editors?

### Q: How to search files?

### Q: How to search in files?

## Managing Processes

### Q: How to display all processes?

### Q: How to get the listen port of a process?

### Q: How to kill processes?

### Q: How to set process priority?

### Q: Running processes in foreground and background?

## III. Programming with Shell Script

## Shell Scripts Basics

### Q: What is the first line in a shell script?

## Variables

## Input and Output

## Control Flow

## IV. Linux System Administrator

## Administration and Configuration

## Managing Software

## Managing User Accounts

### User Accounts

### Q: How to create a system user?

### Q: How to get basic information of system users?

### Q: How to modify system users?

### Q: How to delete system users?

### User Groups

### Q: How to get basic information of system groups?

### Q: How to create a system group?

### Q: How to modify system groups?

## Managing Disk and Filesystems

## V. Linux Server Administrator

## Networking

## Services

### Q: What is initialization system (init)?

### Q: What is systemd?

### Q: How to write unit configuration files of systemd?

### Q: What are basic commands of systemd?

## Configuring Server

## Troubleshooting Linux

## VI. Linux Security

## Firewall

### Q: What is firewall?

### Q: How to use ufw to set firewall?



## References

Books

- Linux Bible
- The Linux Command Line
- Linux Pocket Guide