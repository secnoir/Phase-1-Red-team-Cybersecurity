
NAT stands for network address translation , We are all familiar to ips such as 192.168.x.x , 10.0.x.x , 172.16.x.x etc. We might think these are the addresses that the internet sees but no these are actually private addresses used only locally. When we want to send data across the internet we use a public ip. Usually most home networks share one single shared public ipv4 address. When the data leaves the Local network by router NAT translates the private ip to a public ip , a public ip could look something like 54.21.16.200 , when there are multiple devices communicating with the internet we might think if we have one shared public ip couldn't it get mixed up when data arrives. PAT solves this problem it assigns a source port to each device when they are communicating with the internet it would look like :
Device 1 : 54.21.16.200:41000
Device 2 : 54.21.16.200:42000
Device 3 : 54.21.16.200:43000

The router keeps these as the translation Table so it knows what device recieves the packets correctly when they arrive.

PAT stands for Port address translation.

The purpose of private ips : 
There is not enough public ips to assign to every device on the internet , to solve this problem we use private ips and only one public ip for a network.