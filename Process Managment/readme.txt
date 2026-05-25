Process Management:
      jobs, bg, fg, nice, nohup

jobs : show active jobs
bg   : resume jobs to background
fg   : resume jobs to the foreground

    bg %jobid : to resume specific with job with id
    fg %jobid : to resume specific with job with id
    kill %jobid : to terminate the process

nice : -20 to 19 (the lower the no. more priority) need super user or permission
     
     -to see nice value : run a job and then stop it 
            to get PID :  ps -ef | grep <job-name>
       to see nice value : ps -l <PID-of-uperjob>

     -new process (low priority)      : nice -n 10 <process>
     -new process (high priority)     : sudo nice -n -5 <process>
     -existing process (PID 1234)     : sudo renice 10 -p 1234

nohup : keep running the process even after clode the terminal
     nohup <process> &
     nohup makes a log file "nohup.out" you can trake going this file
     nohup <process-path> >/dev/null 2>&1 &       not save any log in that file
