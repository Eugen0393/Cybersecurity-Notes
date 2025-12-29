# Section: Intro to LAN
**Path:** Pre-Security  
**Date:** December 29,2025  
**Platform:** TryHackMe  

## 1. Introducing LAN Topologies  
There are different network architectures, and when we refer to the term "topology," we mean the visual layout of the network in question. Below, we will discuss the advantages and disadvantages of these topologies.

* **Star Topology:**

The basic principle of a star topology is that devices are connected to each other through a central network device, such as a switch or hub.
![star-topology](../../images/star-topology.png)
In this topology, data is sent through a central device to which all other devices are connected. Below, we will consider some of the advantages and disadvantages of this topology:
### Star Topology: Pros and Cons

| Advantages | Disadvantages |
| :--- | :--- |
| **Reliability:** If one cable fails, only that device is affected. | **Central Failure:** If the central switch/hub fails, the whole network goes down. |
| **Scalability:** Very easy to add or remove devices without disrupting the network. | **Cost:** Requires more cabling compared to Bus topology. |
| **Management:** Centralized control makes it easier to troubleshoot. | **Hardware:** Requires extra hardware (a central switch or hub). |  



* **Bus Topology:**

This type of connection is based on a single connection known as a trunk cable.

Since all the data travels along a single cable, the data transfer speed slows down very quickly, creating a "bottleneck." This bottleneck also makes it significantly more difficult to find and resolve any malfunctions that may occur.
  
* **Ring Topology:** 
