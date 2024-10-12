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
This returned  `Current permissions of "/challenge/pwn"` and `Needed permissions of "/challenge/pwn"`.  
Changed all the permissions to the following:  
```
chmod u+rw,g+rw,o+rw /challenge/pwn
chmod u+x,g+x /challenge/pwn
chmod o-r,o-w,o-x /challenge/pwn
chmod g-r /challenge/pwn
chmod g+r,o+rx /challenge/pwn
chmod u-r,u-w,g-r,g-w,o-r,o-w /challenge/pwn
chmod u+rw,o+rw /challenge/pwn
chmod u-r,u-w,u-x,g-r,g-w,g-x /challenge/pwn
```
It asked me to make `/flag` readable so gave the command `chmod a=r /flag`  
`cat /flag` to obtain the flag. 

# Permission Setting Practise
Ran `/challenge/run` to get started.  
This returned  `Current permissions of "/challenge/pwn"` and `Needed permissions of "/challenge/pwn"`.  
Changed all the permissions to the following:  
```
1)  chmod u-rw,g+w,g-rx,o+x,o-rw /challenge/pwn
2)  chmod u+rwx,g+rwx,o-rwx /challenge/pwn
3)  chmod u+w,u-x,g-r,g-x,o-r,o-w /challenge/pwn
4)  chmod u-w,g+x,o+r /challenge/pwn
5)  chmod u-r,g+r,g+w,g+x,o-r,o+w,o-x /challenge/pwn
6)  chmod u+rw,o+r,o-w /challenge/pwn
7) chmod u-r+x,g-rw+x,o+w /challenge/pwn
```
I could not move to round 8 as I was unable to find the required permission.  

# The SUID Bit
I used the `chmod` command to set the SUID bit: `chmod u+s /challenge/getroot`.  
Then `/challenge/getroot` to run the program followed by `cat /flag` to obtain the flag.  






