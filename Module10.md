# Untangling Users

# Becoming root with su
Ran the `su` command and gave the password`hack-the-planet`.  
`cat /flag` to get the flag.  

# Other Users with su
Ran the `su zardus` command to change the user to `zardus` and gave the password`dont-hack-me`.   
`/challenge/run` to get the flag.  

# Cracking Passwords
As mentioned, The leaked password hash for zardus was located in `/challenge/shadow-leak`.  
Ran `john /challenge/shadow-leak` to get the password with was `aardvark`.  
Used the `su zardus` command to switch the user.  
Entered the cracked password when prompted.   
`/challenge/run` to get the flag.  

# Using sudo
Run `sudo cat/flag` to obtain the flag.  




