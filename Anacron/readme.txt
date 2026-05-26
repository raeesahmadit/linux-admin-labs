Anacron: is a Linux utility executes scheduled tasks even if the
         system is not running continiously, best for systems which can run 24/7
         exm: you system off on job time so when ever it will start it will check and run the job

check it : /etc/anacrontab
         : rpm -qa | grep anacron       (Redhat Centos)
         : dpkg -l | grep anacron       (Ubuntu)

install : yum/ apt install anacron

to make a anacron job : sudo vi /etc/anacrontab
                        days delay job-name path of script
                        15 5 triger-r /Desktop/name.sh

to check your an jobs : sudo anacron -f -d
                        show every jobs you made

to run anacron now : anacron -fdn 

to see the anacron logs : cd /var/log/syslog (ubuntu)
                          cd /var/log/cron   (CentOs)

we can use anacron :    daily system backup
                        weekly log file cleaning
                        monthly reports generation
                        software updates
                        database maintenance