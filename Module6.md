# Practicing Piping

# Redirecting output
Run `echo PWN > COLLEGE` to obtain the flag

# Redirecting more output
Commands:  `/challenge/run > myflag` followed by `cat myflag` to get the flag.

# Appending output
`/challenge/run >> /home/hacker/the-flag` then `cat /home/hacker/the-flag` to get the flag.

# Redirecting errors
Learnt about the File Descriptor (FD) which is a number that describes a communication channel in Linux.  
Commands used : `/challenge/run > myflag 2> instructions` followed by `cat myflag` to get the flag.

# Redirecting input
Run `echo COLLEGE > PWN` which redirects to `PWN`.  
Followed by `/challenge/run < PWN` to get the flag.

# Grepping stored results
Run `/challenge/run > /tmp/data.txt` which redirects the output to `/tmp/data.txt`.  
Followed by `grep pwn /tmp/data.txt` to get the flag.  

# Grepping live output
Learnt the usage of the pipe | operator and then ran `/challenge/run | grep pwn` to obtain the flag.  

# Grepping errors
Executed `/challenge/run 2>& 1| grep pwn` to get the flag.

# Duplicating piped data with tee
Executed `/challenge/pwn | tee output | /challenge/college` followed by `cat output` to view the contents of the output file.  
This returned 
```
Usage: /challenge/pwn --secret [SECRET_ARG]
SECRET_ARG should be "0QNn1MHf"
```
Finally ran `/challenge/pwn --secret 0QNn1MHf | /challenge/college` to get the flag. 

# Writing to multiple programs
Commands used to get the flag: `/challenge/hack | tee >(/challenge/the) >(/challenge/planet)`   

# Split-piping stderr and stdout
Commands used to get the flag: `/challenge/hack 2> >(/challenge/the) > >(/challenge/planet) `







