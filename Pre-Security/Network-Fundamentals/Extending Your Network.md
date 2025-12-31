# Extending Your Network  

## 1. Introduction to Port Forwarding

Port forwarding is an essential component for connecting applications and services to the internet. Without port forwarding, applications and services, such as web servers, are only accessible to devices on the same network, as shown in the photo:

<img width="622" height="739" alt="image" src="https://github.com/user-attachments/assets/d4e08970-3865-4292-99f5-ebf41a747291" />  

 ---

In order for a website to be accessible to the public (via the internet), port forwarding must be implemented as shown in the diagram below:  
<img width="1066" height="507" alt="image" src="https://github.com/user-attachments/assets/9f568fc1-0908-4bd4-a99e-96584a8254f6" />  

With this configuration, Network #2 will now be able to access the web server running on Network #1 using Network #1's public IP address (`82.62.51.70`).

---

## 2. Firewalls 101

A firewall is a network device responsible for determining which traffic is allowed in and out. An administrator can configure a firewall to allow or deny traffic in and out of the network based on a variety of factors, such as:

* Where the traffic is coming from? (has the firewall been told to accept/deny traffic from a specific network?)
* Where is the traffic going to? (has the firewall been told to accept/deny traffic destined for a specific network?)
* What port is the traffic for? (has the firewall been told to accept/deny traffic destined for port 80 only?)
* What protocol is the traffic using? (has the firewall been told to accept/deny traffic that is UDP, TCP or both?)

There are several categories of firewalls, for example:  
| Stateful | Stateless |
| ---; | ---; |
