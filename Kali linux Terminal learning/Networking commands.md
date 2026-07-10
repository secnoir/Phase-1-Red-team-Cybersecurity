
ifconfig -> This command shows your ipv4 and ipv6 address if you have it , it also shows your subnet mask , mac address and other network related useful information. 

ip a -> This does everything the ifconfig command does but this is a newer command with a few more features like interface state.

ip route -> It shows your computer's routing table which includes default gateway (router's ip address)  , shows what network interface it should use wlan0 for wifi and eth0 for ethernet , it also shows source ip address which your computer will use when sending packets on that route.

curl ifconfig.me -> This command shows your public ip address.

Nmap -> Nmap is a tool that is used to scan networks to discover devices and services on that network. This is widely used by the cybersecurity community.

* Some common nmap scans are :
* nmap -sS (target ip)      -> This is a syn scan , used to check if tcp ports are open.
* nmap -A (target ip)        -> Also known as aggressive scan , combines multiple scans.
* nmap -sV (target ip)      -> Detects Service versions on open ports
* nmap -O (target ip)        -> Operating system detection
* nmap -Pn (target ip)      -> It assumes host is online and skips host discovery.

ping -> This is a useful tool that is used to test network connectivity and dns resolution. In simple words it is used for network diagnostics. It uses the ICMP (internet control message protocol) which sends an echo request and recieves an echo reply , it then analyzes the results.

traceroute -> This is a tool that shows the path the data packet took from your computer to the destination server.It works by taking advantage of TTL (Time To Live) , it first sends a packet with TTL = 1 , when the packet arrives at the first router TTL gets decremented by 1 causing it to become 0 and router discards the packet and sends ICMP time exceeded message to the sender and traceroute discovers the router's identity. Then it continues the process each time increasing the TTL by 1.This process continues until packet reaches destination.

iwconfig -> the same as ifconfig instead it shows wifi information , ifconfig shows ethernet information.

These two commands enable and disable an interface :
ip link set eth0 up  
ip link set eth0 down

ss -> Used to examine active connections and open ports. This a newer tool that works the same way as netstat but this is newer and more powerful. A common command is ss -tuln , this shows listening tcp and udp ports. This command can used for many other purposes too.

dig -> A tool used for dns lookup , a dns lookup is the process of translating human readable website names into ip addresses. dig is a tool used for detailed dns lookup

nslookup -> The same as dig but the output is much simpler and less detailed.

ip n -> Shows mac address belonging to an ip , it is a newer command and the old command is arp -a , They work the same way.

