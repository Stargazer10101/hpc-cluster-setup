# HPC-cluster-setup

## Description
This repository serves as comprehensive for the initial steps that I performed to setup a HPC CPU cluster .

## Step 1 - Install ssh

### 1.1 Run update for all machines:
sudo apt-get update
Then run:
sudo apt-get upgrade
note: press 'y' if asked

### 1.2 Check ip addr. 
Run:
sudo apt-get install net-tools
then, check ip address using:
ifconfig

You may see something like this:
![](images/ifconfig.png)

This will be used later.

### 1.3 Install ssh server and client on all machines:
Run:
sudo apt-get install openssh-server
then run:
sudo apt-get install openssh-client

### Create the directory .ssh for all machines:
Run:
mkdir ~/.ssh
then run:
chmod 700 ~/.ssh

### 1.5 Generate rsa key for all machines;
Run:
ssh-keygen -t rsa
then, enter the name of rsa file which is inside the directory .ssh
continue to enter the password of rsa file.