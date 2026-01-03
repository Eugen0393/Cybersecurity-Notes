# 1. What is DNS?
The **D**omain **N**ame **S**ystem provides a simple way to connect to devices on the internet without having to remember complex numbers. Every computer on the internet has its own unique address, called an IP address. When you want to visit a website, remembering every IP address is inconvenient, so DNS comes to the rescue. Instead of remembering 104.26.10.229, you can remember google.com.  

---

# 2. Domain Hierarchy

<img width="669" height="483" alt="image" src="https://github.com/user-attachments/assets/420e4764-dcc3-4eb5-95e3-fdc513c7134d" />  


## TLD (**T**op-**L**evel **D**omain) 
This is the rightmost part of the domain name. For example, the top-level domain of google.com is .com. There are two types of top-level domains: $\color{red}{\textsf{gTLDs (Generic Top Level)}}$ and $\color{red}{\textsf{ccTLDs (Country Code Top Domain)}}$. Historically, $\color{red}
{\textsf{gTLDs}}$ were used to indicate to the user the purpose of the domain name; $\color{red}{\textsf{for example, .com was used for commercial purposes, `.org` for organizations, .edu for education, and `.gov` for government}}$. And $\color{red}{\textsf{ccTLDs}}$ were used for
geographic purposes, $\color{red}{\textsf{for example, `.ca` for sites located in Canada, `.co.uk` for sites located in the United Kingdom}}$, and so on. Because of this demand, there has been an influx of new gTLDs, ranging from `.online, .club, .website, .biz`, and many others.


## Second-Level Domain  
Let's take `google.com` as an example. The .com part is the top-level domain (TLD), and google is the second-level domain. When registering a domain name, the second-level domain is limited to 63 characters + the TLD and can only use a-z 0-9 and hyphens (it cannot begin or end with a hyphen, nor can it contain consecutive hyphens).

## Subdomain  
A subdomain is located to the left of the second-level domain and is separated by a period; for example, in the name `admin.google.com`, the admin portion is a subdomain. Subdomain names are subject to the same restrictions as second-level domains. Multiple subdomains separated by periods can be used to create longer names, such as `jupiter.servers.google.com`. However, the length must not exceed 253 characters, and the number of subdomains is unlimited.

# 3. DNS Record Types
DNS isn't just for websites though, and multiple types of DNS record exist.  

## $\color{red}{\textsf{A}}$ Record
These records correspond to IPv4 addresses, such as 104.26.10.229.

## $\color{red}{\textsf{AAAA}}$ Record  
These records are translated into IPv6 addresses, for example, 2606:4700:20::681a:be5

## $\color{red}{\textsf{CNAME}}$ Record
These records resolve to another domain name, effectively acting as an alias. For example, `store.tryhackme.com` points to `shops.shopify.com`.

## $\color{red}{\textsf{MX}}$ Record
These records resolve to the address of the servers handling email for the domain you are querying. For example, the MX record for `tryhackme.com` is `alt1.aspmx.l.google.com`.

## $\color{red}{\textsf{TXT}}$ Record  
TXT records are text fields that can store any text data. TXT records have many uses, but the most common is listing servers authorized to send emails on behalf of a domain (this can help combat spam and spoofed emails).

# What happens when you make a DNS request  
<img width="675" height="553" alt="image" src="https://github.com/user-attachments/assets/a0259bcd-46d5-48fd-8eca-47d4181aa935" />

### 🔄 DNS Resolution Process

1.  **Local Cache**
    Your computer first checks its own memory. If you visited the site recently, the IP address is saved here.

2.  **Recursive DNS Server**
    Usually provided by your ISP. It checks its own cache. If the IP is not found, it starts the search by contacting the Root Server.

3.  **Root Server**
    The backbone of DNS. It doesn't know the specific IP but redirects the request to the correct **TLD Server** (based on the extension like `.com` or `.org`).

4.  **TLD Server (Top-Level Domain)**
    It points to the **Authoritative Name Server** responsible for that specific domain (e.g., `tryhackme.com`).

5.  **Authoritative Server**
    The "Final Boss". It holds the actual DNS records (IP address).
    * It sends the IP back to the Recursive Server.
    * The result is cached for a specific time (**TTL** - Time To Live) to speed up future requests.

```mermaid
graph TD
    User[Your Computer] -->|1. Check Cache| LocalCache
    LocalCache -->|2. If missing| Recursive[ISP Recursive Server]
    Recursive -->|3. Ask| Root[Root Server]
    Root -->|4. Redirect to .com| TLD[TLD Server .com]
    TLD -->|5. Redirect to Nameserver| Auth[Authoritative Server]
    Auth -->|6. Return IP Address| Recursive
    Recursive -->|7. Save TTL & Return IP| User
