Dean Weiss
20 October 2022

# The Pros & Cons of Intrusion Detection System

<p>
   Network Intrusion Systsm (NIDS): Idenitifies incidents and potential threats. It sists off to the side of the network and monitors traffic. When the sensors encounter something that matches up to a previously detected attack signature, they report the activity to the console. Can notify security personnel of infections, spyware or key loggers, as well as accidental information leakage, security policy violations, unauthorized clients and servers, and even configuration errors.
  
  Intrusion Prevention System and Intrusion Detection System are similiar except that IPS are able to block potential threats as well. They monitor, log and report activities, similiarly to an IDS, but also can stop the threats without the system administrator getting involved. If an IPS is not configured correctly, they can deny legitimate traffic as well, so are not suitable for all aplications.
  
  Network Intrusion Detection Systems vs. Host Intrusion Detection Systems: Network-Based (monitoring the ethernet) have a quicker response than host-based sensors and they are also easier to implement. NIDS doesn't need to alter the existing infrastructure and they monitor everything on a network segment, regardless of the target host's operating system. They do not need software loaded and managed at the different hosts in the network, they have a lower cost of setup and ownership.
  
  NIDS can pick up what a HIDS misses because it looks at packets in real time. However, HIDS can pick up what NIDS will miss, such as unathorized users making changes to the system file. HIDS monitors eventsd and audit logs, comparing new entries to attack signatures. It is resource intensive, so additional hardware will need to be planned for.
  
  While NIDS does real-time detection, meaning it can log evidence that an attacker might try to erease and allows for a quicker response time it also turns up more fals positivies than HIDS. 
  
<ul>   
  Pros of NIDS
    <li> - Tuned to Specific Content in Network Packets </li>
    <li> - Look at Data in the Context of the Protocol </li>
    <li> - Can qualify and Quantify Attacks </li>
    <li> - Make it easier to keep up with regulations </li>
    <li> - Boost efficiency </li>
</ul>
<ul>
  Cons of NIDS
    <li> - Will not prevent incidents by themselves </li>
    <li> - Experience Engineer is Needed to Administer Them </li>
    <li> - Do not Process Encrypt Packets </li>
    <li> - IP Packets can be Faked </li>
    <li> - False Positives are Frequent </li>
    <li> - Susceptible to Protocol Based Attacks </li>
   <li> - Signature Library Needs to be Continually Updated to Detect the Latest Threats </li>
 </ul>
</p>
