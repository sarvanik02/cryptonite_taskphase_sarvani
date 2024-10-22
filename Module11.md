# CHAINING COMMANDS

# Chaining with semicolons
The task was to chain two commands, `/challenge/pwn` and `/challenge/college`, using a semicolon `(;)`  
Commands used to receive flag : `/challenge/pwn; /challenge/college`  

# Your First Shell Script
The task was to create a shell script named `x.sh` to execute two commands, `/challenge/pwn` and `/challenge/college`, sequentially.  
Commands used: `echo "/challenge/pwn;/challenge/college" > x.sh` and `bash x.sh`  

# Redirecting Script Output  
The task was to create a shell script named `x.sh` that executes the commands `/challenge/pwn` and `/challenge/college`  
Ran `bash x.sh | /challenge/solve` to receive the flag.  

# Executable Shell Scripts
Commands used : `echo "/challenge/solve" > x.sh` followed by `chmod a+x x.sh` which changed its permissions to make it executable .  
Flag received by executing `./x.sh`  

