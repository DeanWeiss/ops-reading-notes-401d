Dean Weiss
1 Dec 2022
source: https://www.greycampus.com/blog/information-security/what-is-a-sniffing-attack-and-how-can-you-defend-it

# What Is Sniffing Attack And How Can You Defend Against It

#### Define a Sniffing Attack
This technology can be used to test the telephone lines and determine the quality of the call but criminals used it for their own illegitimate purpose. In the world of internet, sniffing can be performed using an application, hardware devices at both the network and host level. Any network packet having information in plain text can be intercepted and read by the attackers.

Sniffing motives:    
- username an passwords
- Stealing bank related/transaction related information
- Spying on email and chat messages
- Identity theft

#### Types of Sniffing
There are two types of sniffing- active and passive..

##### Passive Sniffing:
This kind of sniffing occurs at the hub. A hub is a device that received the traffic on one port and then retransmits that traffic on all other ports. The sniffer can sit there undetected for a long time and spy on the network.

##### Active Sniffing:
The sniffer will flood the switch with bogus requests so that the CAM table gets full. Once the CAM is full the switch will act as a switch and send the network traffic to all ports. Now, this is legitimate traffic that gets distributed to all the ports. This way the attacker can sniff the traffic from the switch.  

#### Attack Implementations

##### MAC flooding:
Flooding the switch with MAC addresses so that the CAM table is overflowed and sniffing can be done. 

##### DNS cache poisoning:
Altering the DNS cache records so that it redirects the request to a malicious website where the attacker can capture the traffic. The malicious website may be a genuine looking website which has been set up by the attacker so that the victims trust the website. The user may enter the login details and they are sniffed right away.

##### Evil Twin attack:
The attacker uses malicious software to change the DNS of the victim. The attacker has a twin DNS set up already (evil twin), which will respond to the requests. This can be easily used to sniff the traffic and reroute it to the website that the attacker wishes.

##### MAC spoofing:
The attacker can gather the MAC address(s) that are being connected to the switch. The sniffing device is set with the same MAC address so that the messages that are intended for the original machine are delivered to the sniffer machine since it has the same MAC address set.  

#### Protocols vulnerable to sniffing attacks

- HTTP:
Hypertext transfer protocol is used at layer 7 of the OSI model. This is an application layer protocol that transmits the information in plain text. This was fine, when there were static websites or websites that did not required any input from the user. Anyone can set up a MITM proxy in between and listen to all the traffic or modify that traffic for personal gains. Now when we have entered into the web 2.O world, we need to ensure that the user’s interaction is secured. This is ensured by using the secured version of HTTP i.e. HTTPS. Using https, the traffic is encrypted as soon as it leaves layer 7.

- TELNET:
Telnet is a client-server protocol that provides communication facility through virtual terminal. Telnet does not encrypt the traffic by default. Anyone having access to a switch or hub that connects the client and the server can sniff the telnet traffic for username and password. SSH is used as an alternate to the unsecured telnet. SSH uses cryptography to encrypt the traffic and provides confidentiality and integrity to the traffic.  

- FTP:
FTP is used to transfer files between client and server. For authentication FTP used plain text username and password mechanism. Like telnet, an attacker can sniff the traffic to gain credentials and access all the files on the server. FTP can be secured by sung SSL/TLS or can be replaced by a more secured version called SFTP (SSH file transfer protocol). 

- POP:
It stands for Post office protocol and is used by email clients to download the emails form the mail server. It also used plain text mechanism for communication hence it is also vulnerable to sniffing attacks. POP is followed by POP2 and POP3 which are little bit more secure than the original version. 

- SNMP:
Simple network management protocol is used for communication with managed network devices on the network. SNMP uses various messages for communication and community strings for performing client authentication. Community strings in effect are just like password that is transmitted in clear text. SNMP has been superseded by SNMPV2 and V3, v3 being the latest and most secure.


##### Wireshark:
An opensource packet capturer and analyzer. It supports Windows, Linux etc. and is a GUI based tool (alternate to Tcpdump). It used pcap to monitor and capture the packets from the network interface. The packets can be filtered basis IP, protocol and many other parameters. The packets can be grouped or marked basis relevance. Each packet can be selected and dissected as per need (also consider checking this perfect guide for cyber security certification). 

##### dSniff:
It is used for network analysis and password sniffing from various network protocols. It can analyze a variety of protocols (FTP, Telnet, POP, rLogin, Microsoft SMB, SNMP, IMAP etc) for getting the information.
Microsoft network monitor: As the name suggests it is used for capturing and analyzing the network. It is used for troubleshooting the network. Some of the features of the software are Grouping, a Large pool of protocol support(300+), Wireless monitor mode, reassembly of fragmented messages etc.

##### Debookee:
It is a paid tool that can be used to monitor and analyze the network. It is able to intercept and analyze the traffic from devices that are in that subnet, irrespective of the device type (Laptop, devices, TV etc). It offers various modules:


### Precautionary measures against Sniffing attacks

- Connect to trusted networks: Do you trust a free Wi-Fi offered by the coffee shop next door? Connecting to any public network will have a risk that the traffic might be sniffed. Attackers choose these public places exploiting the user’s lack of knowledge. Public networks are setup and then may or may not be monitored for any intrusions or bugs. Attackers can either sniff that network or create a new network of their own with similar names so that the users get tricked into joining that network. An attacker sitting at an airport can create a Wi-Fi with the name of “Free Airport Wi-Fi” and the nearby users may connect to it sending all the data through the attackers’ sniffer node. The word of caution here is that you should only connect to the network you trust – home network, office network etc.   

- Encrypt! Encrypt! Encrypt! : Encrypt all the traffic that leaves your system. This will ensure that even if the traffic is being sniffed, the attacker will not be able to make sense of it. One thing here to be noted is that security work on defense in depth principle. Encrypting he data does not mean that now everything is safe. The attacker might be able to capture a lot of data and run crypto attacks to get something out of it. Use of secured protocols ensures that the traffic is encrypted and renders security for the traffic. Websites using https protocol are more secure than the ones that use HTTP – how is that achieved? Encryption.    

- Network scanning and monitoring: Networks must be scanned for any kind of intrusion attempt or rogue devices that may be setup in span mode to capture traffic. Network admins must monitor the network as well so as to ensure the device hygiene. IT team can use various techniques to determine the presence of sniffers in the network. Bandwidth monitoring is one, an audit of devices which are set to promiscuous mode etc.
