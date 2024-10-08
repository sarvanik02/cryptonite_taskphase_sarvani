# Pondering Paths

# The Root
This challenge required invoking a program called `pwn` located in the root directory `(/)` to capture a flag.  
I invoked the `pwn` program with the following command '/pwn` to receive the flag.  
Flag -> pwn.college{0m5G3NUDChlbSQmo-C37tm5ry8i.dhzN5QDL2kzN0czW}

# Program and absolute paths
The challenge required executing a program called `run`, which is located in the `/challenge` directory.  
Typed the following command to invoke the run program : `/challenge/run`   
Flag -> pwn.college{gJpP1SaznmOr3VZZM8wHlC2ehvA.dVDN1QDL2kzN0czW}

# Position thy self  
The challenge required executing the /challenge/run program from a specific directory.  
Initially tried executing the program with the following commands `cd/home/hacker` followed by `pwd`.  
Received the following error:
`Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.
Please use the `cd` utility to change directory appropriately.`  

Executed the command to change to the required directory: `cd /usr/share/doc/`
Followed by the `pwd` command to confirm successful navigation.  
Flag -> pwn.college{sddPbT_HofhaEgwYInxcG9rqjQS.dZDN1QDL2kzN0czW}  





