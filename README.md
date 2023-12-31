﻿# Linux Classwork

## Create user and set an expiry date
```
useradd kate -e 2023-08-31
```
<img width="281" alt="s1" src="https://github.com/catherine-essien/vals-linux-classwork/assets/136251239/16a41a4a-d5b8-4534-8355-7423ded630b3">

## Prompt user to set password on login
To prompt a user to set a password on each login i used
```
passwd --expire kate
```
<img width="278" alt="s3" src="https://github.com/catherine-essien/vals-linux-classwork/assets/136251239/e2cdd359-3c23-48ce-aa6e-678d3538552f">

### To confirm: 
`chage -l kate`

## Add user to group
Usermod command adds a user to a group. The syntax for the usermod command is: usermod -a -G groupname username.
```
groupadd altschool
usermod -aG altschool kate 
```
<img width="278" alt="s3" src="https://github.com/catherine-essien/vals-linux-classwork/assets/136251239/c04f10a3-978e-4304-a428-52c4415a5500">


## Allow altschool group run cat command on /etc/
add 
```
%altschool ALL=/bin/cat /etc/*
```
to visudo
<img width="393" alt="s4" src="https://github.com/catherine-essien/vals-linux-classwork/assets/136251239/c5e3143f-d796-482b-9fa5-111b3b96d7c4">


## Create user without home directory
I used the command:-M for creating a user without a Home directory, an example is given below
```
useradd -M foo
```
<img width="270" alt="s5" src="https://github.com/catherine-essien/vals-linux-classwork/assets/136251239/9464c3de-b02f-490b-b7e8-a30aa2afd960">

