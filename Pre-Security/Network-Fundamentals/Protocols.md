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
