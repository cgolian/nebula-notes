### Level 02 

Similarly as in Level 01 ```/home/flag02/flag02```, the ```setuid``` bit is set and ```system```call is made in the binary.  
We are going to modify the environmental variable ```USER``` value of which is used in the ```system``` call:  

```USER=$USER && getflag```  
```/home/flag02/flag02 ``` and we're done.  