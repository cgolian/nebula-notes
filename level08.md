### Level 08
After taking a look in ```/home/flag08```        
we find a file (```capture.pcap```) containing a packet dump.  
There are multiple options how this can be analyzed (```tcpdump``` or ```tcpflow```),  
I decided to go with ```tcpflow```:  
```tcpflow -c -r capture.pcap```   
There we can see logged a login attempt for the user ```level08``` - where the password is also entered.

