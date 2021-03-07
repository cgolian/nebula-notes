### Level 00
```find / -type f -perm -4000 -user flag00 2>/dev/null```  
  
Explanation:
* ```-type f``` we are looking for *files*
* ```-perm -4000```   setuid bit is set
* ```-user flag00``` owned by user ```flag00```
* ```2>/dev/null``` we don't care about `Permission denied` error messages
  
Running the above command returns us two results:  
```
/bin/.../flag00
/rofs/bin/.../flag00
```  

After executing ```/bin/.../flag00``` we're asked to run `getflag` and we're done.



