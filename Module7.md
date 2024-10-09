# Shell Variables

# Printing Variables
Run `echo $FLAG` to obtain the flag.

# Setting Variables
Run `PWN=COLLEGE` to obtain the flag.

# Multi-word Variables
Run `PWN="COLLEGE YEAH"` to obtain the flag.

# Exporting Variables
Run `COLLEGE=PWN` followed by `PWN=COLLEGE` then `export PWN` and `sh`.  
Finally execute `/challenge/run PWN` to get the flag.

# Printing Exported Variables
Run the `env` to obtain the flag.

# Storing Command Output
Run `PWN=$(/challenge/run)` which creates a variable `PWN` and assigns a value to it.  
Followed by `echo "$PWN"` to obtain the flag. 

# Reading Input
Run `read PWN` to input values.  
Give `COLLEGE` as the input to get the flag.

# Reading Files
Run `read PWN < /challenge/read_me` to obtain the flag.
