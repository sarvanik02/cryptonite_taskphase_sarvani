# File Globbing

# Matching with *
Ran `cd /ch*` to navigate into the `challenge` directory.   
Executed `/challenge/run` to get the flag.

# Matching with ?
Run cd /?ha??engetook to navigate to thechallenge directory followed by `/challenge/run` which returns the flag.

# Matching with []
Nagivate to `cd /challenge/file` directory  
Followed by `file_[bash]` to get the flag.

# Matching paths with []
Executed `/challenge/run /challenge/files/file_[bash]`.  
Returned the flag. 

# Mixing globs
Run `cd /challenge/files` to navigate into the directory.  
Followed by `ls ?*ing` to match filenames that fit the specific pattern.  
Output:
```
amazing  challenging  laughing  pwning  thrilling  uplifting
```
Ran `/challenge/run [cep]*` to obtain the flag.

# Exclusionary globbing
Simply run ` cd /challenge/files` and then `/challenge/run [^pwn]*` to get the flag. 










