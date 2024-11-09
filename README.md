# Linux 2420 Assignment 2

### Introduction

This assignment involves creating two Bash scripts designed to automate essential system administration tasks in a Unix environment. These scripts will simplify system setup and user management, focusing on best practices for script clarity, error handling, and command-line flexibility.

1. Configuration Scripts: A script to automate the installation of essential software and the linking of configuration files from a remote Git repository.

2. User Creation Script: A script to automate user account creation, including setting up groups, creating home directories, and configuring shell settings.

### Table of Contents




### Project 1: Configuration Scripts

---

Project-1 streamlines the setup of a new system like installing software packages, creating symbolic links to certain files.

#### Folder Content

1. `install_packages`
2. `list_packages`
3. `main_script`
4. `symlink_script`

#### Script Information


### System Setup Configuration Scripts

To run the configuration scripts

* The user must have `sudo` or `root` user priviledges.

* The user must have a appropriate user home directory to clone the repository. 

* Clone the repository below into your user home directory.

>[!NOTE]
This will install both project-1 and project-2 directories

```
https://github.com/Basra97/2420-Assignment-2.git

```
To gain permissions to execute the scripts, copy and run the commands below

```
 sudo chmod u+x ./main_script /.install_packages ./symlink_script
```
### Usage Options Examples

```
Usage: 
  echo "[-t] [-h] [-p] [-c]"
  -t  --two scripts # Execute the two scripts install_packages + symlink_script"
  -h, --help        # Show help"
  -p, --packages    #  Run the install_packages script"
  -c, --symlink     # Executes the symlink_script file
```

To use the usage options above

```
sudo ./main_script -t
```
```
sudo ./main_script -h
```
```
sudo ./main_script -p
```
```
sudo ./main_script -c
```

### Project 2: New User Script

#### Folder Content

1. `new-user_script`

#### Script Information

The  `new-user_script` file is designed to automate the process of creating a new user, this includes setting up a home directory and a user account, specify their shell, assign them a gorup and configuring the user a password. 

### New User Script 

To run the new user script

* The user must have access to `sudo` or `root` user priviledges.

* Clone the repository below into your user home directory.

```
https://github.com/Basra97/2420-Assignment-2.git

```
To gain permissions to run the script, copy the command below

```
 sudo chmod u+x new-user_script
```
To run the command, use the code below. 

``` 
sudo ./new-user_script -u User -s shell(/bin/bash) -g group -i "Information on User"
``` 

```
usage:
  echo "[-u] [-s] [-g] [-h] [-i]"
 -u -username  Username for the new user"
 -s -shell     Shell for the user"
 -g -groups    Add additional groups"
 -h -help      Show Help Information"
 -i -information Information about the user"
  exit 1
```

To use the usage options

`sudo ./new-user_script -u username`
`sudo ./new-user_script -s shell`
`sudo ./new-user_script -g groups`
`sudo ./new-user_script -h help`
`sudo ./new-user_script -i information`

























