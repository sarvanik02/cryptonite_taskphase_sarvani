# Comprehending Commands

#Cat: not the pet, but the command!  
Learnt the usage of the `cat` command which is used to display the contents of a file, combine multiple files, and print their content to the terminal.  
Received the flag by running `cat flag`.  

# Catting absolute paths
Received the flag by specifying cat's arguments as absolute paths.  
Ran the `cat/flag` command. 

# more cat practice
The challenge required retrieving the flag file located in a different directory without using the `cd` command.  
The flag was hidden in the file located at `/usr/share/bug/flag`.  
Ran `cat /usr/share/bug/flag` to receive the flag.

# Grepping for a needle in a haystack
I used the `grep` command to search for the flag inside the file `/challenge/data.txt`, which contained a large amount of text.  
Command used to retrieve the flag: `grep "pwn.college" /challenge/data.txt`   

# Listing files
I listed the files in the /challenge directory to locate the renamed file using the command: `ls /challenge`  
This returned: `15038-renamed-run-17884 and DESCRIPTION.md`  
Finally ran `/challenge/15038-renamed-run-17884` command to retrieve the flag.  

# Touching files
The challenge required creating two files named `pwn` and `college` in the `/tmp` directory, and then running the `/challenge/run` command to retrieve the flag.  
Navigated to the /tmp directory using: `cd /tmp` and created the files with the command `touch pwn college` followed by `ls` to list the contents.  
Executed the command to retrieve the flag: `/challenge/run /tmp/pwn`  

# Removing files
The challenge required the removal of the `delete_me` file from my home directory without using the `cd` command.  
Commands used: `rm ~/delete_me` followed by `ls ~`  
Ran the command to verify the deletion and received the flag: `/challenge/check`  

# hidden files
I navigated to the root directory using: `cd /` followed by `ls -a` to list the contents.  
This revealed the hidden file `.flag-271301273529578`  
Received the flag by running `cat .flag-271301273529578`









