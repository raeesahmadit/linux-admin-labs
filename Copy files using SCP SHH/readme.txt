i am trying to send file from one server to another server by using 
SCP (Secure Copy Protocol)

Steps:
1. install ssh package              : sudo apt/yum install openssh-client openssh-server
2. start ssh                        : sudo systemctl start ssh
3. check status ssh                 : sudo systemctl status ssh
4. send file from S1 to S2          : scp 'filename in S1' 'username'@'ip-addrees':'path in S2 to paste'
5. recive file/folder from S2 to S1 : scp -r 'username'@'ip-address':'path in S1 from copy' 'path in S2 where paste' 

-r : use to copy folder