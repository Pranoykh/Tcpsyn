# Scan Your Local Network for Open Ports

1. Find your local IP range

   ```ipconfig``` For Windows

   ```ifconfig``` For Linux

   <img width="1920" height="972" alt="Screenshot (2)" src="https://github.com/user-attachments/assets/6c0bd594-581c-47d6-922e-74b4c0585bf2" />

   My Ip address is: 192.168.1.3

3. Open Nmap

   Run ```nmap -sS 192.168.1.0/30```

   <img width="1920" height="1014" alt="Screenshot (3)" src="https://github.com/user-attachments/assets/a6260e2d-7bbd-49e7-8df6-e018e2eff212" />

   Based on the Nmap output provided, here are the IP addresses and the open ports found on each host:

   1. Host at 192.168.1.1

        This host has the following open ports:

        * Port 53/tcp (service: domain)

        * Port 80/tcp (service: http)

   2. Host at 192.168.1.2

      This host has no open ports found by the scan. All 1000 scanned ports were closed.

   3. Host at 192.168.1.3

      This host has the following open ports:

      * Port 135/tcp (service: msrpc)

      * Port 139/tcp (service: netbios-ssn)

      * Port 445/tcp (service: microsoft-ds)

      * Port 902/tcp (service: iss-realsecure)

      * Port 912/tcp (service: apex-mesh)

      * Port 7070/tcp (service: realserver)

3. Commonly Associated Services

   * Port 53 (domain):

     This port is dedicated to the Domain Name System (DNS). It's the "phonebook of the internet," translating human-readable domain names (like google.com) into IP addresses that computers use to find each other. Most routers run a DNS service on this port for the local network.

   * Port 80 (http):

     This port is used for Hypertext Transfer Protocol (HTTP), which is the foundation of the World Wide Web. When you type a web address into a browser, it's typically trying to connect to a web server on this port to retrieve the webpage.

   * Port 135 (msrpc):

     This port is used by the Windows Remote Procedure Call (RPC) Endpoint Mapper. It allows client devices to find and communicate with services on a server. It's a fundamental part of Windows networking.

   * Port 139 (netbios-ssn):

     This port is for NetBIOS Session Service over TCP/IP. It is a legacy protocol primarily used for file and printer sharing on older Windows networks. Modern systems use port 445 for this.

   * Port 445 (microsoft-ds):

     This port is used by the Server Message Block (SMB) protocol. It's the modern version of the file and printer sharing service used by Windows machines. It's a crucial component for Microsoft networking, including Active Directory.

   * Port 902 (iss-realsecure):

     While Nmap identified it as iss-realsecure, this port is most commonly associated with VMware ESXi hosts and vCenter Server. It is used for management and communication between virtual machine hosts and their management clients.

   * Port 912 (apex-mesh):

     This port is associated with a protocol called APEX (Application Exchange), an older, now largely deprecated, instant messaging protocol.

   * Port 7070 (realserver):

     This port is often used by streaming media services, such as RealNetworks' RealServer, or other media streaming applications. Some remote desktop software like AnyDesk may also use this port for direct connections.






