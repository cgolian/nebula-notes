### Level 04
As we can see in the code snippet below:
```
if(strstr(argv[1], "token") != NULL) {
  printf("You may not access '%s'\n", argv[1]);
  exit(EXIT_FAILURE);
}
```
the file is checking if we are trying to access a file called `token`.  
The simple solution would be then to rename it.  

We are going to create a hard link pointing to this file... 
```
ln /home/flag04/token /home/level04/linkedtkn
```
...and use it as an argument:
```
/home/flag04/flag04 /home/level04/linkedtkn
```