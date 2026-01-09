# 3. How Web servers work.  

## What is Web Server?

A web server is software that accepts incoming connections and uses the HTTP protocol to deliver web content to its clients. The most common web servers are $\color{red}{\textsf{Apache, Nginx, IIS, and NodeJS}}$. The web server delivers files from a root directory, which is defined in the software settings. For example, Nginx and Apache use the same default location – `/var/www/html` in Linux operating systems, while IIS uses `C:\inetpub\wwwroot` for Windows operating systems.

Example:
If you request the file http://www.example.com/picture.png, it will send the file `/var/www/html/picture.jpg` from its local hard drive.

## Virtual Hosts

Web servers can host multiple websites with different domain names; they use virtual hosts for this purpose. The web server software checks the hostname requested from the HTTP headers and matches it against its virtual hosts $\color{red}{\textsf{(virtual hosts are simply text configuration files)}}$. If a match is found, the correct website will be served. If no match is found, the default website will be served.

Virtual hosts can map their root directory to different locations on the hard drive. For example, $\color{red}{\textsf{one.com}}$ can be mapped to `/var/www/website_one`, and $\color{red}{\textsf{two.com}}$ to `/var/www/website_two`.
