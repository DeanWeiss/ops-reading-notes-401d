Dean Weiss
19 October 2022

# Reverse Proxy
<p> 
  
  #### What is Reverse Proxy? 
  Reverse Proxy is a server that sits in front of web servers and forwards clients ( e.g. web browsers) requests to those web servers. They increase security performance and reliability. 
  
 #### What is a Proxy Server?
  A forward Proxy, often called a Proxy, proxy server or web proxy is a server that sits infront of a group of clience machines. A proxy server acts as a middle-man between the services on the internet and the computers its protecting, it acts as a proxy for those computers. 
      
  - A proxy server can be used to get around the restrictions the limited access some organizations use. 
  - They can also be used for the opposite, and block a group of users from accessing certain sites. 
  - It can increase your anonymity online. Only the IP address of the proxy server will be visible
  
#### How is a Reverse Proxy Server Different?
  A proxy server sits infront of one or more web servers,  intercepting requests from clients. This is different from a forward proxy, where the proxy sits infront of clients. A forward proxy sits in front of a client and ensures that no origin server ever communicates directly with that specific client. On the other hand, a reverse proxy sits in front of an origin server and ensures that no client ever communicates directly with that origin server.
  
#### Benefits of a Reverse Proxy
  - Load Balancing: When a website gets millions of views a day the proxy server can distribute the traffic among different servers.
  - Protection from Attacks: A web site or service never needs to reveal the IP address of their origin servers. Makes it hard to leverage an attack aginst them.
  - Global Server Load Balancing (GSLB): Distributes the traffic to different servers around the world.
  - Caching: It can cache and save data so that connections to it can be made faster.
  - SSL Encryption: It can be configured to decrypt all incoming requests and encrypt all outgoing responses.
  
 Reverse Proxies take intensive software and hardware resources. You can use a cloud product to act as a proxy server for you.
  
source: https://www.cloudflare.com/learning/cdn/glossary/reverse-proxy/
</p>
