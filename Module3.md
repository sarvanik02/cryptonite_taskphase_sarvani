# Comprehending Commands

# Cat: not the pet, but the command!  
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

# An Epic Filesystem Quest
Changed to the root directory: `cd /` followed by `ls` to listed contents to find the HINT file  
Read the contents of the HINT file `cat HINT`  
Clue directed to /opt/radare2/shlr/capstone/suite/benchmark  
Navigated to the directory: `cd /opt/radare2/shlr/capstone/suite/benchmark` follwed by `ls`   
Found the next clue in the INSIGHT file: `cat INSIGHT`    
Clue directed to /opt/angr-management/_internal/jedi/third_party/typeshed/stdlib/3/urlli b
Read the contents of this file with the `cat` command.  
Clue pointed to `/usr/lib/python3/dist-packages/jedi/third_party/typeshed/stdlib/3/http`  
Listed files in that directory using `ls`  
This gave the following output: `MESSAGE  __init__.pyi  client.pyi  cookiejar.pyi  cookies.pyi  server.pyi`  
Read the contents of the `MESSAGE` file with the `cat` command.  
Next clue: `/usr/share/doc/libmagic-mgc`  
Listed the hidden files using `ls -a /usr/share/doc/libmagic-mgc`  
Output : `.POINTER  README.Debian  changelog.Debian.gz  copyright`  
Executed `cat /usr/share/doc/libmagic-mgc/.POINTER`  
Received another clue : `/usr/local/lib/python3.8/dist-packages/trio/_core/__pycache__`  
Listed files: `ls -a/usr/local/lib/python3.8/dist-packages/trio/_core/__pycache__`   
Output : `CUE  __init__.cpython-38.pyc  elf.cpython-38.pyc  macho.cpython-38.pyc  pe.cpython-38.pyc  raw.cpython-38.pyc  universal.cpython-38.pyc`  
Read the `CUE` file: `cat CUE`  
Last clue directed to `/usr/share/racket/pkgs/htdp-lib/2htdp/uchat/compiled`  
Listed and read these files.  
Output: `.TIP  auxiliaries_rkt.dep  auxiliaries_rkt.zo  chatter_rkt.dep  chatter_rkt.zo  server_rkt.dep  server_rkt.zo`  
Read `.TIP` with the following `cat /usr/share/racket/pkgs/htdp-lib/2htdp/uchat/compiled/.TI`    
Finally found the flag. 

# Making directories 
Created a directory named `/tmp/pwn` and a file named `college` within it.  
Commands used : `mkdir /tmp/pwn` followed by `touch /tmp/pwn/college`.  
Confirmed the file's existence: `ls /tmp/pwn`  
Output : `college`  
Executed the command to retrieve the flag: `/challenge/run /tmp/pwn/college`  

# finding files
Ran the following command: `find / -name flag`  
Output: All the possible paths were displayed  
```
1.  /usr/local/share/radare2/5.9.5/flag
2.  /usr/local/lib/python3.8/dist-packages/pwnlib/flag
3.  /opt/aflplusplus/nyx_mode/QEMU-Nyx/tests/tcg/mips/user/ase/msa/float-max-min/flag
4.  /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
5.  /opt/radare2/libr/flag
6.  /nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
7.  /nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
```
Attempted to read the first two paths using the `cat` command, which returned errors indicating that they were directories  
```
cat /usr/local/share/radare2/5.9.5/flag : Is a directory
cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag : Is a directory
```
Successfully retrieved the flag from the third path.

# linking files
I learned how to create symbolic links in Linux using the `ln -s` command, which allows one file or directory to point to another.  
Commands : `ln -s /flag /home/hacker/not-the-flag` followed by `file /home/hacker/not-the-flag` to verify the creation of the file.  
Executed the `/challenge/catflag` to retrive the flag.

























