at : to schedule a job only once , service name : atd

at HH:MM (15:16)
echo "ibtu is learning" >> test.txt 
^d to save the job
atq -List at jobs
atrm # -remove a job

you can give multiple jobs at once 

other formats: 
              at 4:45 AM                102021
              at 4PM +4 days            afer 4 days from now
              at now +5 hours           after 5 hours
              at 9:00 AM MON
              at 9:00 AM tomorrow
              at 10:00 AM next month    same day next month at 10 AM
              at 10:00 AM Nov 30        at 10 AM on 30 November
