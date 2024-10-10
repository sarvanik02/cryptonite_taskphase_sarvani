# Perceiving Permissions

# Changing File Ownership
Commands used : `ls -l /flag` followed by `chown hacker /flag` to change the user.  
`cat /flag` to receive the flag.  

# Groups and Files
Commands used : `ls -l /flag` followed by `chgrp hacker /flag` to change the user.  
`cat /flag` to receive the flag. 

# Fun with Group Names
`id` to display the information.  
Output :
```
uid=1000(hacker) gid=1000(grp14754) groups=1000(grp14754)
```
Ran chgrp `grp14754 /flag` along with `cat /flag` to get the flag.  

# Changing Permissions
Commands used : `ls -l /flag` followed by `chmod go+r /flag` to change the permissions.  
`cat /flag` to receive the flag.  

# Executable Files
Run `ls -l /challenge/run` followed by `chmod a+x /challenge/run`. This is used to add execute permissions to the file or directory for all users.  
`/challenge/run` to receive the flag.  

# Permission Tweaking Practise
Ran `/challenge/run` to get started.  
Output: 
```
Round 0 (of 8)!

Current permissions of "/challenge/pwn": rw-r--r--
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
- the group doesn't have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
- the world doesn't have write permissions
- the world doesn't have execute permissions

Needed permissions of "/challenge/pwn": rw-rw-rw-
* the user does have read permissions
* the user does have write permissions
- the user doesn't have execute permissions
* the group does have read permissions
* the group does have write permissions
- the group doesn't have execute permissions
* the world does have read permissions
* the world does have write permissions
- the world doesn't have execute permissions
```
