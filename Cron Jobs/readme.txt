Cron job : (schedule tasks) used to automate repatative tasks or run a script or command at specific interval
           e.g : backing up files,         running system maintaining,          sending email reports
           it use daemon (background process) called Cron , it keep chaecking silently
           its configration stores in a file named crontab
           name of a service : crond
           but server should be running to make cronjob work

it is user base thing
to edit : crontab -e
to view current : crontab -l
to delete : crontab -r (it will remove all the jobs)

basic format to make a cronjob:
    1. crontab -e 
    2. * * * * * /home/ibtu/Desktop/test/script.sh      (all five stars withut value mean every minute)
             explain: min hour day month day of week command
                       *   *    *     *      *
              (0-59) (0-23) (1-31) (1-12) (0-7)(sunday is 0 or 7) 
            or use cronjob.guru online
       and save 

example:  
    0 0 * * * (12 midnight daily)
    30 8 1 * * (1st of every month, 8:30 am)
    */15 * * * * (every 15 min)
    15 14 * * 1-5 (2:15 pm monday to friday)
    15 14 * * MON-FRI
    0 20 10,20,30 2 *   (use , to mention every 10 days in month)

special strings : @reboot, @daily, @hourly, @yearly, @annually, @monthly, @weekly, etc..
             : @reboot /path/script.sh (run scriot at reboot)

use Environment Variable can also be use in cronjob

make a log file of cronjob: * * * * * /home/ibtu/Desktop/test/script.sh > /home/ibtu/Desktop/test/cronlog1.txt 2>&1

to see cronjob logs : /var/log/syslog (ubuntu)