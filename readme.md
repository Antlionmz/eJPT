Documenting the eJPT journey.
Sites used: INE training, Tryhackme
----------
Tryhackme rooms:
Web fundamentals
How DNS works in detail
How HTTP works in detail
Wreath (final exam prep)
--------------
Cheatsheet-like guide:

Tools (that I used) not included in the INE training:
autorecon         #An absolute time saver, must get not just for eJPT but for OSCP!
cherrytree        #one-note like note taking tool. very useful


Pivot:
ip route show
ip add <network1> via <ip1> dev <device>
ip del <network1> via <ip...>
#Most linux-level routers only take one route per network. use ip del to get rid of the conflicting networks.
#Check wireshark pcap file to speculate the network to pivot to, then use tracert from a different machine to determine the router.

  
#Use fping (don't forget to pipe garbage info to devnull) to construct a target ip list, use autorecon to complete the reports.
#This is the optimal strategy although it might not be the one that helps you learn the most - remember to look at the command files in the reports!

  
  

...to be completed
