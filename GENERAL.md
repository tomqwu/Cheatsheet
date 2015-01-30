# Generate Javacore
1. Get PID
watch "ps -eo pcpu,pid,user,args | sort -k 1 -r | head -6" 
or
ps -ef | grep WebSphere
or
cat /opt/WebSphere/AppServer/profiles/AppSrv01/logs/WC_stgmall1/WC_stgmall1.pid
2. kill -3 PID
3. find / -name "*javacore*"

# Pulling logs by scheduler
/workbench/ihs_logs_swap/

e.g. 
[wcsprdsa@prdschldr ihs_logs_swap]$ rsync -vut prdweb01:/opt/WebSphere/IBMIHS/logs/access_log.*.gz /workbench/ihs_logs_swap/prdweb01


# Forwarding X11 packages in prdweb01 via scheduler
## first connect to scheduler server
```bash
ssh -X tom.wu@hostname
ssh –X tom.wu@prdweb01
su - root
```
# grep a string out of files printing only the file name
grep -H "<ErrorMessage>" SystemOut*.log -R | cut -d: -f1

# Check global file write permission security
for PART in `awk '(!/^#/ && $6 != "0") { print $2 }' /etc/fstab 2>/dev/null`; do find $PART -xdev -type f \( -perm -0002 -a ! -perm -1000 \) -print 2>/dev/null; done

# check large file
find . -type f -size +50000k -exec ls -lh {} \; | awk '{ print $9 ": " $5 }'

# extension
# change from one to another
for f in *.php4; do mv $f `basename $f .php4`.php; done;
# add
for f in *; do mv $f `basename $f `.txt; done;
# remove
for f in *.txt; do mv $f `basename $f .txt`; done;

#  AIX 
tar -cvf - /some/directory/path/ | gzip -c | split -b 500m - file.tgz.

# fine and sort
find -type f -print0 | xargs -r0 stat -c %y\ %n | sort

# find file newer than another file and cp
find . -name "*.xml" -newer SKU_1408619449286_557746.xml -exec cp {} /data/full_local/ \;

# find archive and list files
find . -name "daily_archive.20140*.gz" -exec tar ztvf {} \; > /tmp/find.log
