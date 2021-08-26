### Level 10 

```
if(access(argv[1], R_OK) == 0) {
  ...
  ffd = open(file, O_RDONLY);
}
```
The two syscalls differ - `access` uses the real (so not effective) `UID` of the process,  
`open` uses the effective `UID`.  
