1. ipconfig
Purpose: Shows our computer’s IP configuration.
What it does:
•	Displays IP address, subnet mask, default gateway
•	Shows network adapters (Wi-Fi, Ethernet, virtual adapters)
•	Helps diagnose local network issues
2. Netstat -a
netstat -a
Purpose: The netstat -a command is used to display all active and listening network connections on a system.
What it does:
•	Lists all open ports and active connections (both incoming and outgoing)
•	Shows listening ports along with associated protocols (TCP/UDP)
3. netstat
Purpose: Displays active network connections and ports.
What it does:
•	Shows open TCP/UDP connections
•	Displays listening ports
•	Can show the process ID (PID) using each connection

4. ping
ping google.com
Purpose: Tests connectivity between our computer and another host.
What it does:
•	Sends ICMP echo requests
•	Measures response time (latency)
•	Shows packet loss

6. tracert (Traceroute)
tracert google.com
Purpose: Shows the path packets take to reach a destination.
What it does:
•	Lists each router (hop) between the source and the destination
•	Shows delay at each hop
•	Helps identify where network delays or failures occur

7. arp -a
Purpose: Displays the ARP (Address Resolution Protocol) cache.
What it does:
•	Maps IP addresses to MAC addresses
•	Shows devices our PC has recently communicated with on the local network

8. nslookup
nslookup www.google.com
Purpose: nslookup is used to query DNS servers to find IP addresses or domain names.
What it does:
•	Finds the IP address of a domain or the domain name of an IP (forward and reverse lookup).
•	Allows querying specific DNS servers and shows whether the response is authoritative or cached.

9. route print
Purpose: route print is used to display the computer’s current network routing table.
What it does:
•	Shows all active network routes, including destinations, gateways, and interfaces.
•	Helps troubleshoot how network traffic is directed and which route it will take.


10. Host 
host google.com
Purpose :
The host command is used to perform DNS lookups and find the IP address or related DNS records of a domain.
What it does:
•	Resolves a domain name (like google.com) into its corresponding IP address (A/AAAA records).
•	Retrieves DNS information such as mail servers (MX), name servers (NS), and other records for the domain.

 
11. Hostname
hostname
Purpose : The hostname command is used to display or set the name of a computer on a network.
What it does:
•	Shows the current system’s network name (host name)
•	Allows changing or configuring the host name (with proper permissions)

 
 
12. netstat -u
netstat -u — Displays active UDP (User Datagram Protocol) network connections and listening ports on the system.
•	Shows all UDP sockets currently in use
•	Helps identify which services are listening on UDP ports
•	Useful for network troubleshooting and monitoring UDP traffic
13. Windows CMD equivalent of netstat -u:
netstat -an -p UDP
Purpose: Displays active UDP connections and listening UDP ports on Windows.
•	-a → Shows all active connections and listening ports 
•	-n → Displays addresses and ports numerically 
•	-p UDP → Filters results to only UDP protocol


