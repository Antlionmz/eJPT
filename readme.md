Documenting the eJPT journey.
-------------
Tryhackme rooms:
Web fundamentals
How DNS works in detail
How HTTP works in detail
Wreath (final exam prep)
--------------
Sites used: INE training, Tryhackme
Major credits to Kensec: https://kentosec.com/2019/08/04/how-to-pass-the-ejpt/ 
I won't cover the parts that he already did. Plenty of similar resrouces - but here are some of the nooks and crannies not mentioned in any resources I came across.
Cheatsheet-like guide:

Tools included in the INE training:

nmap              #Not just for network scanning/footprinting, but also for vulnerability scanning with scripts.
metasploit        #I held out using this for a while but it is necessary for smb exploits. You can use Searchsploit to avoid using metasploit.

Tools (that I used) not included in the INE training:
autorecon         #An absolute time saver, must get not just for eJPT but for OSCP!
- This is all you need 90% the time. It takes a while so just let it run in the background, check out the reports when it is done.
- Exam the commands sections of the report if you don't understand the output
- Often you will find the vulnerability straight away with this, use Metasploit to follow up.
- Use fping (don't forget to pipe garbage info to devnull) to construct a target ip list, use autorecon to complete the reports.

cherrytree        #one-note like note taking tool. very useful
dirserach         #better dirbuster
------------
Operation Cycle: Enumeration - Exploitation - Exfiltration - Post-exploitation
#Ideally you will only need the first 2 in eJPT. It is by nature not a hard exam but a confidence booster
-------------------------

Pivot:
ip route show
ip add <network1> via <ip1> dev <device>
ip del <network1> via <ip...>
#**Most linux-level routers only take one route per network.** use ip del to get rid of the conflicting networks.
#Check wireshark pcap file to speculate the network to pivot to, then use tracert from a different machine to determine the router.  
#Don't waste too much time on bruteforcing the machines (same as OSCP). Most problems can be solved via enumeration only.
-----------------------
