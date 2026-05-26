netstat (network statistics): network monitoring and troubleshooting
          it is command-line network utility
  disply : network connections for TCP , UDP
           routing table
           a number of network interface
           network protocol statistics

to check no of connections on a port/ip : netstat -putan | grep <port-id>
to see all sockets : netstat -a
to see all TCP ports : netstat -at
to see all TCP v6 ports : netstat -6at
to see all UDP ports : netstat -au
to see all listing ports : netstat -l
to see the numeric addresses : netstat -ln
to see PID of connection : netstat -p
to see the routing table : netstat -r
to see list of interfaces : netstat -i
to see which port a process is using : netstat -ap | grep <process-name>
to see statistics by protocol : netstat -s
