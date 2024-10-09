# Processes and Jobs

# Listing Processes
Ran `ps aux` command which listed all the processes.  
Ran `/challenge/32310-run-16816` out of all the processes to get the flag.

# Killing Processes
Ran `ps -e` which lsited all the processes and `kill 73`  
Ran `/challenge/run` to obtain the flag.  

# Interrupting Processes
Run `/challenge/run` followed by `ctrl+c` which interupts the process and returns the flag.

# Suspending Processes
Ran `/challenge/run` which gave me the following output.  
```
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!
I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
```
Used `ctrl+z` followed by /challenge/run to obtain the flag.  

# Resuming Processes
Ran `/challenge/run` followed by `fg` to get the flag.

# Backgrounding Processes
Executed the command `/challenge/run` to interupt the process followed by `bg /challenge/run` to run the command in the backgroud.
Finally executed `/challenge/run` to get the flag.

# Foreground Processes
Followed the same first step as the previous challenge.  
Then ran `fg /challenge/run` to run it in the foregroud and got the flag.

# Backgrounding Processes
Ran `/challenge/run` which interrupts the process followed by `bg /challenge/run` to run it in the backgroud.  
Executed `/challenge/run` to obtain the flag.

# Starting Backgrounded Processes
Ran`/challenge/run &` which started the background processes and returned the flag.

# Process Exit Codes
Ran `/challenge/get-code` to retrive the exit code.  
Then `echo $?` which gave `108` as the output.  
Finally ran `/challenge/submit-code 108` to obtain the flag.  















