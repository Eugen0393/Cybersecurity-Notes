# Section: The OSI Model & Protocols

---

## 1. Packets vs. Frames
Data changes its form depending on which layer it is traveling through.

* **Encapsulation:** Think of it like a Russian doll or an envelope. We wrap data inside headers to protect and direct it.
* **Packet (Layer 3):** Contains the **IP Address**. It acts like the "Letter" that knows the final destination.
* **Frame (Layer 2):** Contains the **MAC Address**. It acts like the "Envelope" that handles the delivery to the next immediate device.

---

## 2. TCP vs. UDP (Transport Layer)
Layer 4 controls *how* the data is delivered.

* **TCP (Transmission Control Protocol):** Connection-based and reliable. It checks for errors and guarantees the file arrives perfectly (Full Cat). Used for emails and browsing.
* **UDP (User Datagram Protocol):** Stateless and fast. It shoots data without checking if it arrived (Broken Cat). Used for video streaming and gaming where speed is more important than perfection.

---

## 3. The TCP Three-Way Handshake
Because TCP is reliable, it must "introduce" the devices before sending data.

<img width="471" height="493" alt="image" src="https://github.com/user-attachments/assets/369c754e-3849-4680-ad81-e50b935d20f7" />

* **SYN:** The client sends a request to synchronize ("Hello, can we talk?").
* **SYN/ACK:** The server acknowledges and agrees ("Yes, I am ready").
* **ACK:** The client confirms the connection ("Okay, sending data now").

## 4. Ports 101
Because port numbers can range from 0 to 65535, it's easy to lose track of which application is using which port. Fortunately, we associate applications, software, and behavior with a set of standard rules. For example, by ensuring that web browser data is transmitted over port 80, software developers can create web browsers like Google Chrome or Firefox that interpret the data identically.  

Any port in the range from 0 to 1024 is known as a normal port. Below are some examples:

| Protocol | Port | Description |
| :--- | :---: | :--- |
| **FTP** (File Transfer Protocol) | 21 | Used for file sharing between computers. Allows you to upload or download files. |
| **SSH** (Secure Shell) | 22 | Used to securely log in to systems remotely via a command line (text-based interface). |
| **HTTP** (HyperText Transfer Protocol) | 80 | The standard protocol for the Web. Used by browsers to load pages, images, and videos (Unsecured). |
| **HTTPS** (HTTP Secure) | 443 | The secure version of HTTP. Does the exact same thing as port 80 but uses **encryption** to protect data. |
| **SMB** (Server Message Block) | 445 | Used for sharing files and printers on a local network (Very common in Windows). |
| **RDP** (Remote Desktop Protocol) | 3389 | Allows you to connect to a remote computer and use its graphical desktop (GUI), unlike SSH which is text-only. |
