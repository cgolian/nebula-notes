### Level 05    
The file we are looking for is just hidden:
```
ls -la  
cp /home/flag05/.backup/backup-19072011.tgz /home/level05/.  
cd /home/level05
gunzip backup-19072011.tgz
tar -xvf backup-19072011.tar
```