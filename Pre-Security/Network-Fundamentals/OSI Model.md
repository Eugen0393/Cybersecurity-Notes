# What is the OSI Model?
It is a model that provides a framework that defines how all network devices will send, receive, and interpret data.
<img width="568" height="445" alt="image" src="https://github.com/user-attachments/assets/37ea03c8-0d5f-452b-98d8-b9276f8ce342" />  
Each level performs its own set of functions and is located from Layer 7 to Layer 1.  

* **Application:** These are familiar everyday applications that we use every day, for example, FileZilla, Gmail, which provide a convenient **graphical user interface** (GUI) for users to interact with the data sent or received.

# 

* **Presentation:** This is the level at which standardization begins. While software developers can create any piece of software, such as an email client, in different ways, data must still be processed the same way—regardless of how the software operates.

`In short, this level functions as a translator.`

# 

* **Session:** This layer is responsible for connecting and maintaining a session with the device to which data needs to be sent.

# 

* **Transport:** At this level, it is determined which of the two protocols, TCP or UDP, is best used to transmit the required data. TCP is best when the data needs to arrive intact, without losing any fragments, while UDP is more suitable for streaming, video, and other applications, where the loss of certain fragments is less of a concern.
<img width="970" height="400" alt="image" src="https://github.com/user-attachments/assets/6453b045-63ac-485a-997b-96ff0b23edc1" />

<img width="897" height="339" alt="image" src="https://github.com/user-attachments/assets/347e787b-3e15-47fd-bfd2-a9c51d51f59f" />

# 

* **Network:** This is the routing layer that directs pieces of data to the right devices, simultaneously determining the most optimal path along which these pieces of data should be sent, using protocols such as OSPF (**Open Shortest Path First**) and RIP (**Routing Information Protocol**)
<img width="977" height="463" alt="image" src="https://github.com/user-attachments/assets/c4900c7a-ecfc-434d-b47b-b8d70e0aac5c" />

# 

* **Data Link:** The data link layer focuses on the physical addressing of transmitted data by adding a physical MAC address


# 

* **Physical:** Devices use electrical signals to transmit data to each other in binary (1's and 0's) via Ethernet cables.
<img width="592" height="437" alt="image" src="https://github.com/user-attachments/assets/a3d3049c-9c47-496e-ac1c-00efef7f159d" />
