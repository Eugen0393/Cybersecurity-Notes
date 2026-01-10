# 1. Putting It All Together
In short, when you request a website, your computer needs to know the IP address of the server it needs to communicate with; it uses DNS for this purpose. Then your computer communicates with the web server using a special set of commands called the HTTP protocol; the web server returns HTML, JavaScript, CSS, images, etc., which your browser then uses to properly format and display the website.  
<img width="739" height="174" alt="image"   src="https://github.com/user-attachments/assets/b972f345-93ca-4368-8028-69f4e80fb6da" />  

There are also several other components that help the website function more efficiently and provide additional features.  



# 2. Load Balancers  
Load balancers are needed to prevent overloading already busy web servers, and they also provide redundancy in case a server stops responding. When you send a request to a web server, your request first goes to the load balancer, which then redirects it to one of several servers behind it. The load balancer uses various algorithms to determine which server is best suited to handle the request. For example: `round-robin`, $\color{red}{\textsf{which sends the request to each server in turn}}$, or the `Weighted` algorithm, $\color{red}{\textsf{which checks how many requests a server is currently handling and sends the request to the least loaded server}}$.  
<img width="611" height="321" alt="image" src="https://github.com/user-attachments/assets/62a775e8-fa93-49b7-8130-0e997e1b79b0" />  


Load balancers also perform periodic checks with each server to ensure they are running correctly; this is called a $\color{red}{\textsf{health check}}$. If a server doesn't respond appropriately or doesn't respond, the load balancer will stop sending traffic until it responds appropriately again.

## CDN (**C**ontent **D**elivery **N**etworks)  
A CDN can be an excellent tool for reducing the load on an overloaded website. **It allows you to host your website's static files, such as JavaScript, CSS, images, and videos, on thousands of servers worldwide.**  

## Databases  
Websites often need a way to store information for their users. Web servers can interact with databases to store and retrieve data. Databases can range from a simple text file to complex clusters of multiple servers providing speed and fault tolerance, **such as MySQL, MSSQL, MongoDB, Postgres, and others**; each of them has its own specific features.

## WAF (**W**eb **A**ppliccation **F**irewall)  
**A WAF (Web Application Firewall) sits between your web request and the web server; its main task is to protect the web server from hacking or denial-of-service attacks.** It analyses the web requests for common attack techniques, whether the request is from a real browser rather than a bot. It also checks if an excessive amount of web requests are being sent by utilising something called rate limiting, which will only allow a certain amount of requests from an IP per second. If a request is deemed a potential attack, it will be dropped and never sent to the webserver.  
<img width="612" height="177" alt="image" src="https://github.com/user-attachments/assets/4b488e68-d135-4226-b2a4-f4237a0aacaa" />
