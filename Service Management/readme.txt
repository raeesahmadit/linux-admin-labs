a service is always continous running in background and track externaly

1. systemctl : use to control the status of a service

    to start      : systemctl start ssh
    to stop       : systemctl stop ssh
    to see status : systemctl status ssh
    to restart    : systemctl restart ssh

2. sudo systemctl enable <service-name>: 
       use to start a service always even after restart but admin rights needed
         no need always start it 

       to enable and start at same time : sudo systemctl enable --now ssh
       to see status                    : sudo systemctl is-enable ssh
       service not start after reboot   : sudo systemctl disable ssh

3. (MASKING) to prevent a service to start from any user : 
              apply         : sudo systemctl mask ssh
              check         : sudo systemctl unmask ssh 

4. Computer control:
       to shutdown : systemctl poweroff
       to reboot   : systemctl reboot / reboot
       to forcefully reboot user : systemctl -i reboot (ignoring logged-in user)

5. list the sockets in memory avaliable for IPC (interprocess comunnication):
       to see sockets : systemctl list-sockets
       to see types   : systemctl --show-types list-sockets

6. to see running service : systemctl | grep -i running