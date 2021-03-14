### Level 06
"legacy Unix system" 
Wikipedias entry on ```/etc/passwd``` mentions  
``` 
Prior to password shadowing, a Unix user's hashed password was stored in the second field of their record in the /etc/passwd file (within the seven-field format as outlined above).
```
Let's take a look what we can find for the user ```flag06```
``` 
cat /etc/passwd | grep flag06
```
We'll use ```john the ripper``` to try and recover the original password from the hash:   
```
echo "ueqwOCnSGdsuM" > candidates.txt
john candidates.txt --show
```
