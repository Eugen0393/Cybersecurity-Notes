# 3. How Web servers work.  

## What is Web Server?

A web server is software that accepts incoming connections and uses the HTTP protocol to deliver web content to its clients. The most common web servers are $\color{red}{\textsf{Apache, Nginx, IIS, and NodeJS}}$. The web server delivers files from a root directory, which is defined in the software settings. For example, Nginx and Apache use the same default location – `/var/www/html` in Linux operating systems, while IIS uses `C:\inetpub\wwwroot` for Windows operating systems.

Example:
If you request the file http://www.example.com/picture.png, it will send the file `/var/www/html/picture.jpg` from its local hard drive.
