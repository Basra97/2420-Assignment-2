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
  -h, --help          # Show help"
  -p, --packages    #  Run the install_packages script"
  -c, --symlink      # Executes the symlink_script file
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




