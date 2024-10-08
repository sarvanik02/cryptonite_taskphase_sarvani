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
```
Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.
Please use the cd utility to change directory appropriately.
```
Executed the command to change to the required directory: `cd /usr/share/doc/`  
Followed by the `pwd` command to confirm successful navigation.  
Flag -> pwn.college{sddPbT_HofhaEgwYInxcG9rqjQS.dZDN1QDL2kzN0czW}  

# Position elsewhere
Initially tried executing the program with the following commands: `cd /usr/share/doc/` followed by `pwd`
Received the following error:
```
Incorrect...
You are not currently in the /usr/share/zoneinfo/posix/Asia directory.
Please use the `cd` utility to change directory appropriately.
````
After encountering the error, I executed the command to change to the required directory: `cd /usr/share/zoneinfo/posix/Asia` followed by `pwd`.  
Once I was in the correct directory, I ran the program with `/challenge/run`  
Flag -> pwn.college{IS-rpwzKfAhVHHNUzwbVhD9oXGs.ddDN1QDL2kzN0czW}

# Position yet elsewhere
Initially, I tried to execute the program from an incorrect directory `cd /usr/share/zoneinfo/posix/Asia`.  
Received the following error message:
```
Incorrect...
You are not currently in the /sys/kernel directory.
Please use the `cd` utility to change directory appropriately.
```
Changed to the required directory: `/sys/kernel`.  
Used the `pwd` command to confirm successful navigation followed by `/challenge/run` to run the program.  
Flag -> pwn.college{U2TADtnZgrM97nNfLw895MQ-ymX.dhDN1QDL2kzN0czW}


# implicit relative paths, from /
Executed the command to change to the root directory : `cd / ` followed by `pwd` to verify successful navigation.  
Executed this `challenge/run` to run the program.  
Flag -> pwn.college{gI4pXOOmuRLVVSKWHpQOEEuuuDM.dlDN1QDL2kzN0czW}

# explicit relative paths, from /
The challenge was to run the `/challenge/run` program using a relative path that includes `.` to show the current directory.  
I changed to the root directory with the command `cd /` followed by `pwd`.   
I ran the run program using the relative path: `./challenge/run`
Flag -> pwn.college{Ys0FFPhcO7FfXY1NKJx7yyMX1Ne.dBTN1QDL2kzN0czW}

# Implicit relative path
The challenge was to run the run program from the `/challenge` directory.
I navigated to the /challenge directory by entering `cd /challenge` followed by `pwd` to confirm successful navigation.  
Executed the run program with the command `./run` to receive the flag.  
Flag -> pwn.college{M7RGT_A_B7bAy0sqSALdnf146LK.dFTN1QDL2kzN0czW}

# Home sweet home
The challenge required running the `/challenge/run` program with an argument that specifies where to write the flag.
Initially tried to run the program with `cd /home/hacker/asdf` and `/challenge/run /home/hacker/f` which did not work.  
Had to use ChatGPT for help and I tried to use . (dot) to indicate the current directory, but I realized that I needed to specify an actual filename instead.  
Decided to use the filename c, which is three characters or less as specified.  
Executed the commands `/challenge/run ~/c` to receive the flag.  
Flag -> pwn.college{IOSJMkUNLx4YvMw5c-JDoxQTy7F.dNzM4QDL2kzN0czW}










