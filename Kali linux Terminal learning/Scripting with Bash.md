This is going to be my first scripting with bash ever. I will be making a beginner ping sweep script.

SCRIPT : 

for ip in $(seq 1 254) ; do
      ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" & 
done

What it does :
This is a ping sweep script that basically sends ICMP echo request to all the ips on a network subnet and shows which ips are active or online. This script uses for loop , it only sends 1 packet per ip just to check if the host is alive. The grep "64 bytes" gives the output of the specific line that contains 64 bytes , the cut tool cuts the rest of the words on the line and lands on the 4th word and shows it , in this case we get output 192.168.0.119: , we want to remove the ":" so we use that last command tr which then gives us a clean output of 192.168.0.119

As i progress i will be making the script better each time.

How we can run this script :

first we need to give it the execute permission by doing -> chmod +x ipsweep.sh

then we can run it simply like -> ./ipsweep.sh 192.168.0 

if you want the output in a file you can do -> ./ipsweep.sh 192.168.0 > ip.txt

We have to give an ip range so it knows exactly what octet is should scan.

BETTER SCRIPT : 

#!/bin/bash

if [ "$1" == "" ]
then
echo "You forgot an ip address"
echo "Syntax: ./ipsweep.sh 192.168.1"

else
for ip in $(seq 1 254) ; do
      ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" & 
done
fi


What it does now : 

for the script to run successfully you need to specify the ip range it should scan for example , ./ipsweep.sh 192.168.0 , this scans the 4th octet of this ip address from 1 to 254. If we run the command as ./ipsweep.sh it wouldn't work because it doesn't know what ip to scan.
For this purpose if a person doesn't know or forgets to put an ip it prints the following text :
"You forgot an ip address "
"Syntax: ./ipsweep.sh 192.168.0"

Lets say we saved the output of this scan in a file "iplist.txt" and we want to run nmap scan on all of them. We could directly run a one line bash script in the terminal such as :

for ip in $(cat iplist.txt); do nmap  -sS -p 80 -T4 $ip & done

This scans all the ips saved in the iplist.txt using nmap all at once. it does a stealth scan on port 80.