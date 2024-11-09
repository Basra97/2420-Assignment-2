# Linux 2420 Assignment 2

### Introduction

This assignment involves creating two Bash scripts designed to automate essential system administration tasks in a Unix environment. These scripts will simplify system setup and user management

1. Configuration Scripts: `project-1` automates the installation of essential software and the linking of configuration files from a remote Git repository.

2.  New User Script: `project-2` is used to automate user account creation, including setting up groups, creating home directories, and configuring the users shell settings.

## Project 1: Configuration Scripts

---

### Folder Content

1. `list_packages`
2. `install_packages`
3. `symlink_script`
4. `main_script`


### Script Information

`project-1` streamlines the setup of a new system like installing software packages, creating symbolic links to certain files.

The `list_packages` file contains the packages that need to be added by the system.

The `install_packages` is used for the installation of the software packages (`kakoune` and `tmux`)

The `symlink_script` file creates symbolic link for config files such as ~/.config/kak/kakrc and ~/.bashrc. Symbolic links act as a shortcut to files or directories. 

The `main_script` calls both `install_packages` and `symlink_script` 

### User Requirements 

>[!NOTE]
These scripts are designed for an Arch Linux environment.

* The user must have access to `sudo` or `root` user privileges.

* The user also needs `git` installed to clone the remote repository.

You can download git with the following command

```
sudo pacman -S git  # For Arch Linux users

```

>[!NOTE]
 This project requires a dependencies.
 fzf is a text selctor and fzf is used in the .bashrc file  which is used in our `symlink_script` file.


To install `fzf`, copy and run the following command


  ``` 
  sudo pacman -Syu fzf
  ```


### System Setup Configuration Scripts

To run the configuration scripts

* The user must have `sudo` or `root` user privileges.

* The user must have an appropriate user home directory to clone the repository. 

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

To use the usage options see below

> **Important**: Must use sudo to run command

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

## Project 2: New User Script

---

### Folder Content

1. `new-user_script`

### Script Information

`project-2` contains a script file that creates new users. 

The  `new-user_script` file is designed to automate the process of creating a new user, this includes setting up a home directory and a user account, specify their shell, assign them a group and configuring the user a password. 

### User Requirements 

>[!NOTE]
These scripts are designed for an Arch Linux environment.

- The user must have access to `sudo` or `root` user privileges.

### New User Script 

To run the new user script you must use `sudo` or `root`

* Clone the repository below into your user home directory if you haven’t already.

```
https://github.com/Basra97/2420-Assignment-2.git

```
To gain permissions to run the script, copy the command below

```
 sudo chmod u+x new-user_script
```

To run the command, use the code below. 

> **Important**: Must use sudo to run command


``` 
sudo ./new-user_script -u User -s shell(/bin/bash) -g group -i "Information on User"
``` 
>[!NOTE]
 Replace username, group, and "User Information" with the appropriate details for the new user.

### Usage Options Examples

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


* To use the usage options


```sudo ./new-user_script -u username```

```sudo ./new-user_script -s shell```

```sudo ./new-user_script -g groups```

```sudo ./new-user_script -h help```

```sudo ./new-user_script -i information```






















