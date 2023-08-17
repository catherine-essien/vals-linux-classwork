# Linux Classwork

## Create user and set an expiry date
`useradd kate -e 2023-08-31`

## Prompt user to set password on login
`passwd --expire kate`
### To confirm: 
`chage -l kate`

## Add user to group
```
groupadd altschool
usermod -aG altschool kate 
```

## Allow altschool group run cat command on /etc/
add `%altschool ALL=/bin/cat /etc/*` to visudo

## Create user without home dir
`useradd -M foo`