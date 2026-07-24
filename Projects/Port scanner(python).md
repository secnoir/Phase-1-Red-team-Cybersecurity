#!/bin/python3

import socket

def scan_port(target, port):
    sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    sock.settimeout(1)
    
    try:
        result = sock.connect_ex((target, port))
        return result == 0  # True if open, False otherwise
    finally:
        sock.close()  # Always close

target = "scanme.nmap.org"  # A safe target to practice on

print(f"Scanning {target}...")
for port in range(20, 81):  # Scan ports 20-80
    if scan_port(target, port):
        print(f"[+] Port {port} is OPEN")