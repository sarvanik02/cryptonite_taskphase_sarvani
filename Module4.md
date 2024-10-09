# DIGESTING DOCUMENTATION
# Learning from documentation
Ran the command `/challenge/challenge --giveflag` to get the flag.

# Learning Complex Usage
The goal was to retrieve the flag by using the `/challenge/challenge` program, which required passing the `--printfile` argument along with the file path to the flag.  
Command executed to obtain the flag: `/challenge/challenge --printfile /flag`

# Reading Manuals
Commands used : `man challenge`  
This returned a manual with a description which said
```
 Output the flag when called with the right arguments.
--yxjicm NUM
              print the flag if NUM is 066
```
Obtained the flag with `/challenge/challenge --yxjicm 066`.  

# Searching Manuals
Executed `man challenge` along with `/flag` to find the find.  
It stated that `--osezu` contains the flag.  

# Searching for Manuals
Executed `man challenge` along with `man -k challenge!` to find the find.
This returned `rvlnbbwwtk (1)       - print the flag!`  
Executed `man rvlnbbwwtk` which returned the number `342`  
Finally executed `/challenge/challenge --rvlnbb 342` to get the flag.  

# Helpful Programs
Ran `/challenge/challenge --help` to view the documentation. 
Output:
```
-h, --help: Show help message and exit.
--fortune: Read your fortune.
-v, --version: Get the version number.
-g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG: Get the flag if given the correct value.
-p, --print-value: Print the value that will cause the -g option to give you the flag.
```
Used `/challenge/challenge --p` to find the secret value which was 642  
Finally executed `/challenge/challenge -g 642` to retrieve the flag.

# Help for Builtins
Ran the command `help challenge` to view the documentation.  
Output: 
```
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value is "Uw396Vcg".
```
Ran `challenge --secret Uw396Vcg` to obtain the flag.  

