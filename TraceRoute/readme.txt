TraceRoute: Trace the route how data travels on internet from your pc to destination

install : sudo apt install traceroute

   -default package is 60byte to change          : traceroute www.google.com 100
   -default no of package per hop is 3 to change : traceroute -q 1 www.google.com   (hops mean routers between destinations)
   -default port is 33434 to change              : traceroute -p 21101 www.google.com
   -to use IPv6 or IPv4                          : traceroute -4/-6 www.google.com
   -to route through gate                        : traceroute -g 192.168.10.68 www.google.com
