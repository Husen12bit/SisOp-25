# TUGAS SISTEM OPERASI MINGGU KE-2

---

![Image](https://github.com/user-attachments/assets/838b068c-4d85-452a-aca6-352d279fbd3f)

#### Dosen Pengampu :
**Dr. Ferry Astika Saputra ST, M.Sc**

#### Disusun oleh :
**Muhammad Abdullah Husaini**
**(3214521030)**
D3-LA IT-A

---

1. 
    >**QUESTION :**
    >
    >What are the three main purpose of an operating system?

    >**ANSWER :**
    >
    >1.	Resource Management
    >2.	Abstraction and Simplification
    >3.	User Interface and System Control

---

2.	
    >**QUESTION :**
    >
    >We have stressed the need for an operating system to make efficient use of the computing hardware. When is it appropriate for the operating system to forsake this principle and to "waste" resources? Why is such a system not really wasteful?

    >**ANSWER :** 
    >
    >Because there are things that are more/must be prioritized such as user I/O. Data security and periodic checking of virus attacks, needs when making videos/images/animations/effects or just to enhance user experience satisfaction that must be done in order to achieve ease, security, user efficiency according to the conditions that apply at that time.

---

3. 
    >**QUESTION :**
    >
    >What is the main difficulty that a programmer must overcome in writing an operating system for a real-time environment?

    >**ANSWER** :
    > 
    >How many are there and I will take the case of the control tower at the airport where programmers are required to be able to create a system that can act quickly, responsively, without delay even when given a heavy and non-stop workload.

---

4. 
    >**QUESTION :**
    >
    >Keeping in mind the various definitions of operating system, consider whether the operating system should include applications such as web browsers and mail programs. Argue both that it should and that it should not, and support your answers!

    >**ANSWER :** 
    >
    >on the one hand (the pros) if an operating system is made into an application or even a Gmail link is:
    >>1.	cyber security is more guaranteed
    >>2.	Functions and objectives are focused so that it makes it easier for users/admins
    >>3.	so that it can improve user experience
    >
    >But there are several disadvantages such as:
    >>1.	More memory and system resource usage
    >>2.	each publication from a different company will produce different features and look views which can actually confuse users

---

5. 
    >**QUESTION :**
    >
    >How does the distinction between kernel mode and user mode function as a rudimentary form of protection (security)?

    >**ANSWER :**
    >
    >Kernel mode and user mode actually have significant differences such as in the field of system execution, ownership of access to software and hardware and also security protection, namely kernel mode because its access ownership covers most of the computer components, so when there is a crash or system damage it will affect all computer components while user mode because its access is limited, the damage caused does not affect all parts.

---

6. 
    >**QUESTION :**
    >
    >which of the following instructions should be privileged?
    >- A. Set value of timer		
    >- B. Read the clock		
    >- C. Clear memory		
    >- D. Issue a trap instruction	
    >- E. Turn off interrupts
    >- F. Modify entries in device-status table
    >- G. Switch From user to kernel
    >- H. Access I/O device

    >**ANSWER :**
    >
    >- A. Set value of timer
    >- B. Clear memory 
    >- E. Turn off interrupts
    >- F. Modify entries in device-status table 
    >- G. Switch From user to kernel
    >- H. Access to I/O device

---

7. 
    >**QUESTION :**
    >
    > Some early computers protected the operating system by placing it in a memory partition that could not be modified by either the user job or the operating system itself. Describe two difficulties that you think could arise with such a scheme

    >**ANSWER :**
    >
    >The problem is if the operating system cannot be modified, updated or given additional patches because any changes required to the operating system will require a complete system reboot or a more complicated process to replace the entire operating system image. Then, in addition, this restraint also makes resource allocation inefficient due to its less effective use.

---

8. 
    >**QUESTION :**
    >
    >Some CPUs provide for more than two modes of operation. What are two possible uses of these multiple modes?

    >**ANSWER :**
    >
    >The first is to allow for improved isolation and data security as well as protection against malicious software. Then the PC can also be optimized for performance such as Advanced caching or parallel processing that can achieve energy efficiency and provide better performance.

---

9. 
    >**QUESTION :**
    >
    >Timers could be used to compute the current time. Provide a short description of how this could be accomplished.

    >**ANSWER :**
    >
    >1.	Hardware Clock
    >2.	Timer Interrupts
    >3.	Timekeeping
    >4.	Synchronization
    >5.	User Access

---

10. 
    >**QUESTION :**
    >
    >Give two reasons why caches are useful. What problems do they solve? What problems do they cause? If a cache can be made as large as the device for which it is caching (for istance, a cache is large as a disk), why not make it that large  and eliminate the device

    >**ANSWER :**
    >
    >Why Caches Are Useful:
    >>-	Speed Improvement
    >>- Reduced Workload on Main Storage
    >
    >Problems Caches Solve:
    >>- Performance Bottlenecks
    >>- High Latency for Repeated Accesses
    >
    >Problems Caches Cause:
    >>- Cache Coherency
    >>- Cache Misses
    >>- Complexity and Cost
    >
    >Why Not Make the Cache as Large as the Device?:
    >>- Cost
    >>- Power Consumption
    >>- Diminishing Returns
    >>- Physical Size

--

11. 
    >**QUESTION :**
    >
    >Distinguish between the client-server and peer-to-peer models of dis-tributed systems

    >**ANSWER :
    >
    >1.	**Architecture**
    >>- *In the client-server model, there is a clear separation between the client and the server. The client sends requests, while the server provides services or resources. The server functions as the central management hub. In contrast, in the peer-to-peer (P2P) model, all nodes (peers) have equal roles. Each peer can function as both a client and a server, sharing resources and services directly without a central authority.*
    >2.	**Scalability**
    >>- *Scalability can be a challenge in the client-server model because the server can become a bottleneck as the number of clients increases. Adding more clients requires scaling up the server's capacity. On the other hand, P2P is more scalable because the load is distributed among all peers. Adding new peers increases the overall capacity and performance of the system.*
    >3.	**Resource Management**
    >>- *In the Client-Server model, resource management is centralized. The server is responsible for managing data, resources, and access control, which can simplify administration but also creates a single point of failure. In P2P, resource management is decentralized. Each peer manages its own resources and shares them with other peers, which can enhance redundancy but also make resource discovery and management more challenging.*
    >4.	**Fault Tolerance**
    >>- *In the Client-Server model, if the server fails, clients cannot access services, resulting in a single point of failure. Redundancy can be implemented, but it requires additional infrastructure. In contrast, P2P is generally more fault-tolerant. If one peer goes offline, other peers can still communicate and share resources, making the system more resilient to failures.*

---

12. 
    >**QUESTION:
    >
    >How do clustered systems differ from multiprocessor systems? What is required for two machines belonging to a cluster to cooperate to provide a highly available service?

    >**ANSWER:**
    >
	>**Differences Between Clustered Systems and Multiprocessor Systems:**
    >1.	**Architecture:**
    >
    >>- **Multiprocessor Systems:** *Multiple processors (CPUs) share the same physical memory and are tightly coupled, often within a single machine or motherboard.*
    >>- **Clustered Systems:** *Multiple independent machines (nodes) are connected via a network and work together. Each machine has its own memory and resources.*
    >2.	**Communication:**
    >>- **Multiprocessor Systems:** *Processors communicate through shared memory, which is fast and efficient.*
    >>- **Clustered Systems:** *Nodes communicate over a network, which is slower compared to shared memory but allows for greater scalability and geographic distribution.*
    >3.	**Scalability:**
    >>- **Multiprocessor Systems:** *Limited by the number of processors that can be physically integrated into a single system.*
    >>- **Clustered Systems:** *Highly scalable, as additional nodes can be added to the network to increase capacity.*
    >4.	**Fault Tolerance:**
    >>- **Multiprocessor Systems:** *A failure in the shared memory or system bus can bring down the entire system.*
    >>- **Clustered Systems:** *More fault-tolerant, as the failure of one node does not necessarily affect others.*
    >5.	**Cost and Complexity:**
    >>- **Multiprocessor Systems:** *Expensive to build and maintain due to the complexity of shared memory and inter-processor communication.*
    >>- **Clustered Systems:** *Generally cheaper and easier to scale, as they use off-the-shelf hardware and standard networking.*
    >
    >**Requirements for Two Machines in a Cluster to Cooperate for High Availability:**
    >1.	**Network Connectivity:**
    >>- *The machines must be connected via a reliable and high-speed network to communicate and synchronize data effectively.*
    >2.	**Shared Storage or Data Replication:**
    >>- *The machines need access to shared storage (e.g., a SAN) or must replicate data across nodes to ensure consistency and availability.*
    >3.	**Cluster Management Software:**
    >>- *Specialized software is required to manage the cluster, monitor node health, and handle failover. Examples include Kubernetes, Apache Hadoop, or Microsoft Failover Clustering.*
    >4.	**Failover Mechanism:**
    >>- *A failover mechanism must be in place to automatically transfer workloads from a failed node to a functioning one, ensuring minimal downtime.*
    >5.	**Synchronization and Coordination:**
    >>- *The machines must synchronize their states and coordinate tasks to avoid conflicts and ensure consistency. Protocols like Paxos or Raft can be used for distributed consensus.*
    >6.	**Load Balancing:**
    >>- *A load balancer or distributed scheduling mechanism is needed to distribute workloads evenly across the nodes, optimizing resource utilization.*
    >7.	**Monitoring and Recovery:**
    >>- *Continuous monitoring of node health and automated recovery processes are essential to detect failures and restore services quickly.*

---

13. 
    >**QUESTION**
    >
    >Consider a computing cluster consisting of two nodes running a database. Describe two ways in which the cluster software can manage access to the data on the disk. Discuss the benefits and disadvantages of each.

    >**ANSWER**
    >
    >**Shared Disk Architecture**
    >
    >*In this model, both nodes in the cluster have direct access to the same shared storage. The data on the disk is accessible to all nodes simultaneously.*
    >>Benefits:
    >>- Simplified Data Management 
    >>- High Availability 
    >>- Load Balancin
    >
    >>Disadvantages:
    >>- Single Point of Failure
    >>- Performance Bottleneck
    >>- Complexity in Coordination
    >
    >**Shared Nothing Architecture:**
    >
    >*In this model, each node has its own private storage, and data is partitioned across the nodes. Each node is responsible for managing its own subset of the data.*
    >>Benefits:
    >>- Scalability
    >>- No Single Point of Failure
    >>- Better Performance
    >
    >>Disadvantages:
    >>- Complex Data Partitioning
    >>- Data Redundancy
    >>- Query Coordination
---

14. 
    >**QUESTION**
    >
    >What is the purpose of interrupts? How does an interrupt differ from a trap? Can traps be generated intentionally by a user phgram? If so, for what purpose?

    >**ANSWER**
    >
    >Interrupts function to enable the handling of synchronous events, improve CPU utilization, facilitate real-time processing, manage multitasking, enable device communication, handle errors, and enhance system responsiveness.
    >
    >Traps are generated by the CPU itself in response to certain conditions during program execution. These can be caused by errors (such as division by zero, invalid memory access) or specific instructions like system calls, which are intended for error handling, debugging, and system calls.

---

15. 
    >**QUESTION**
    >
    >Explain how the Linux kernel variables HZ and jiffies can be used to determine the number of seconds the system has been running since it was booted.

    >**ANSWER**
    >
    >The number of seconds the system has been running since boot can be calculated using the formula:
    >>Seconds = jiffies/HZ
    >
    >- jiffies: The total number of timer interrupts since the system was booted.
    >- HZ: The frequency of timer interrupts per second.

---

16. 
    >**QUESTION**
    >
    >Direct memory access is used for high-speed I/O devices in order to avoid increasing the CPU's execution load.
    >- a. How does the CPU interface with the device to coordinate the transfer?
    >- b. How does the CPU know when the memory operations are com-plete?
    >- C. The CPU is allowed to execute other programs while the DMA controller is transferring data. Does this process interfere with the execution of the user programs? If so, describe what forms of interference are caused.

    >**ANSWER**
    >
    >***a.	How does the CPU interface with the device to coordinate the transfer?***
    >1.	**Initialization:**
    >>- The CPU sets up the DMA controller by providing it with the necessary information, such as:
    >>>- The memory address where data should be read from or written to.
    >>>- The number of bytes to transfer.
    >>>- The direction of the transfer (read or write).
    >>- This is typically done through memory-mapped I/O or port-mapped I/O.
    >2.	**Handoff to DMA Controller:**
    >>- Once the DMA controller is configured, the CPU hands off control of the data transfer to the DMA controller.
    >>- The CPU can then continue executing other tasks while the DMA controller handles the data transfer.
    >3.	**Device Interaction:**
    >>- The DMA controller communicates directly with the I/O device and memory, coordinating the transfer of data without further CPU intervention.
    >

    >***b.	How does the CPU know when the memory operations are complete?***
    >1.	**Interrupt Notification:**
    >>- When the DMA controller completes the data transfer, it sends an interrupt to the CPU to signal that the operation is finished.
    >>- The CPU then handles the interrupt and performs any necessary post-transfer tasks, such as updating data structures or notifying the requesting process.
    >2.	**Polling (Less Common):**
    >>- In some systems, the CPU may periodically check the status of the DMA controller by reading a status register. However, this approach is less efficient and rarely used in modern systems.
    >

    >***c.	The CPU is allowed to execute other programs while the DMA controller is transferring data. Does this process interfere with the execution of the user programs? If so, describe what forms of interference are caused.***
    >
    >Yes, DMA can interfere with the execution of user programs, but the interference is generally minimal. The main forms of interference are:
    >1.	**Memory Bus Contention:**
    >>- Both the CPU and the DMA controller share the same memory bus. If the DMA controller is actively transferring data, it may temporarily block the CPU from accessing memory, causing slight delays in program execution.
    >>- This is known as cycle stealing, where the DMA controller "steals" memory cycles from the CPU.
    >2.	**Cache Coherency Issues:**
    >>- If the CPU uses a cache, data modified by the DMA controller may not immediately reflect in the CPU's cache, leading to stale data. This requires cache invalidation or write-back mechanisms to maintain coherency.
    >3.	**Interrupt Handling Overhead:**
    >>- When the DMA transfer completes, the interrupt generated by the DMA controller may cause a context switch, temporarily pausing the execution of user programs.
    >4.	**Resource Contention:**
    >>- If multiple DMA devices are active simultaneously, they may compete for memory bandwidth, further increasing contention and potentially slowing down the system.

---

17. 
    >**QUESTION**
    >
    >Some computer systems do not provide a privileged mode of operation in hardware. Is it possible to construct a secure operating system for these computer systems? Give arguments both that it is and that it is not possible.

    >**ANSWER**
    >- ***Possible:***
    >>1.	**Software-Based Protection Mechanisms:**
    >>*Even without hardware-supported privileged mode, an OS can implement security mechanisms in software*
    >>2.	**Language-Based Security:**
    >>*Use programming languages with built-in safety features (Rust, Java, dll) to enforce security at the application level*
    >>3.	**Microkernel Architecture:**
    >>*A microkernel design minimizes the amount of code running in privileged mode, reducing the attack surface. Even without hardware support, a small, well-audited kernel can enforce security policies.*
    >- ***Not possible:***
    >>1.	Lack of Hardware Enforcement
    >>2.	Complexity and Trust
    >>3.	Inability to Prevent Privilege Escalation

---

18. 
    >**QUESTION**
    >
    >Many SMP systems have different levels of caches; one level is local to each processing core, and another level is shared among all processing cores. Why are caching systems designed this way?

    >**ANSWER**
    >
    >To reduce memory latency and also manage cache coherence to facilitate the implementation of coherence protocols.

---

19. 
    >**QUESTION**
    >
    >Rank the following storage systems from slowest to fastest:
    >1. Hard-disk drives
    >2. Registers
    >3. Optical disk
    >4. Main memory
    >5. Nonvolatile memory
    >6. Magnetic tapes
    >7. Cache

    >**ANSWER**
    >
    >1.	Magnetic tapes **(slowest)**
    >2.	Optical disk 
    >3.	Hard-disk drives 
    >4.	Nonvolatile memory   
    >5.	Main memory 
    >6.	Cache 
    >7.	Registers **(fastest)**

---

20. 
    >**QUESTION**
    >
    >Consider an SMP system similar to the one shown in Figure 1.8. Illustrate with an example how data residing in memory could in fact have a different value in each of the local caches.

    >**ANSWER**
    >
    >In an SMP system, multiple processors share memory but have their own caches. Without proper cache coherence, data in memory can have different values in each cache. For example:
    >>1. Initial State: Memory location X = 10.
    >>2. P1 Reads X: Caches X = 10.
    >>3. P2 Reads X: Caches X = 10.
    >>4. P1 Writes X = 20: Updates memory but fails to invalidate P2's cache.
    >>5. P2 Reads X: Gets stale value 10 from its cache.
    >
    >Result: Memory has X = 20, but P1's cache has 20 and P2's cache has 10.

---

21. 
    >**QUESTION**
    >
    >Discuss, with examples, how the problem of maintaining coherence of cached data manifests itself in the following processing environments
    >- a. Single-processor systems 
    >- b. Multiprocessor systems 
    >- c. Distributed systems

    >**ANSWER**
    >
    >**a.	Single-Processor System:**
    >1. Manifestation:
    >>- The main issue is between the CPU cache and I/O devices using DMA.
    >>- Changes to main memory by DMA can cause the CPU cache to become stale.
    >2. Example:
    >>- A network card writes packet data to memory via DMA.
    >>- If the CPU has a copy of that data in its cache, the copy becomes invalid.
    >3. Solution:
    >>- Cache flushing or memory bus snooping.
    >
    >**b.	Multiprocessor System:**
    >1. Manifestation:
    >>- Multiple processors/cores share main memory, each with its own local cache.
    >>- Changes to data in one cache make other caches inconsistent.
    >2. Example:
    >>- CPU 1 and CPU 2 read the same variable into their caches.
    >>- CPU 1 modifies the variable.
    >>- CPU 2's cache becomes stale.
    >3. Solution:
    >>- Cache coherence protocols.
    >
    >**c.	Distributed System:**
    >1. Manifestation:
    >>- Each node has its own memory and local cache.
    >>- Issues arise when multiple nodes access and store the same data, especially in DSM or distributed file systems.
    >2. Example:
    >>- Node A and Node B store the same file from a distributed file system.
    >>- Node A modifies the file.
    >>- Node B's cache becomes stale.
    >3. Solution:
    >>- Distributed cache coherence protocols, distributed file system protocols, and data versioning mechanisms.

---

22. 
    >**QUESTION**
    >
    >Describe a mechanism for enforcing memory protection in order to prevent a program from modifying the memory associated with other programs.

    >**ANSWER**
    >
    >1.	**Memory Management Unit (MMU):**
    >>- Translates virtual addresses (used by programs) to physical addresses (actual memory).
    >>- Ensures programs only access their allocated memory.
    >2.	**Virtual Memory:**
    >>- Each program has its own isolated virtual address space.
    >>- The OS maps virtual addresses to physical memory using page tables.
    >3.	**Page Table Entries (PTEs):**
    >>- Each PTE contains permission bits (read, write, execute).
    >>- The MMU checks these bits during memory access. If a program violates permissions (e.g., writing to read-only memory), the MMU triggers a fault.
    >4.	**Kernel and User Modes:**
    >>- Programs run in user mode and cannot access kernel memory or other programs' memory.
    >5.	**Fault Handling:**
    >>- If a program tries to access unauthorized memory, the OS terminates it or handles the error.

---

23. 
    >**QUESTION**
    >
    >Which network configuration-LAN or WAN-would best suit the following environments?
    >- a.	A campus student union
    >- b.	Several campus locations across a statewide university system
    >- c.	A neighborhood

    >**ANSWER**
    >
    >a.		A campus student union
    >>best: **LAN**
    >
    >b.	Several campus locations across a statewide university system
    >>best: **WAN**
    >
    >c.	A neighborhood
    >>best: **LAN**

---

24. 
    >**QUESTION**
    >
    >Describe some of the challenges of designing operating systems for mobile devices compared with designing operating systems for traditional PCs.

    >**ANSWER**
    >
    >**Challenges of Designing Mobile OS :**
    >1.	Resource Constraints:
    Limited battery, memory, storage, and processing power.
    >2.	Power Management:
    Must extend battery life.
    >3.	User Interface:
    Small screens and touch-based input.
    >4.	Connectivity:
    Frequent switching between Wi-Fi and cellular networks.
    >5.	Security:
    Vulnerable to theft, loss, and malware.
    >6.	App Ecosystem:
    Must support diverse apps and hardware.
    >7.	Updates:
    Need frequent, seamless updates.
    >8.	Multitasking:
    Limited resources for multitasking.
    >9.	Hardware Diversity:
    Many device types and configurations.
    >10.	Always-On Features:
    Requires continuous background processing.

---
25. 
    >**QUESTION**
    >
    >What are some advantages of peer-to-peer systems over client-server systems?

    >**ANSWER**
    >
    >- In a client server system, the server is a bottleneck
    >- In a peer to peer system, service can provide by several nodes distributed throughout the network

---

26. 
    >**QUESTION**
    >
    >Describe some distributed applications that would be appropriate for a peer-to-peer system

    >**ANSWER**
    >
    >1.	**skype** : voice call or video call using a technology  voice over IP(VoIP)
    >2.	**danamas** : connecting borrowers with investors
    >3.	**Napster** : a centralized server maintened an index of al files stored on peer nodes in the napster network, and the actual exchange of files took place between the peer nodes

---

27. 
    >**QUESTION**
    >
    >Identify several advantages and several disadvantages of open-source operating systems. Identify the types of people who would find each aspect to be an advantage or a disadvantage

    >**ANSWER**
    >
    >**Advantages of Open-Source OS:**
    >1. Customizability: Modify the OS to fit specific needs.
    >>- Who Benefits: Developers, tech enthusiasts.
    >2. Cost: Free to use.
    >>- Who Benefits: Budget-conscious users, small businesses.
    >3. Transparency: Inspect and verify the source code.
    >>- Who Benefits: Security experts, privacy-focused users.
    >4. Community Support: Collaborative development and help.
    >>- Who Benefits: Users who prefer community-driven solutions.
    >5. Innovation: Access to cutting-edge features.
    >>- Who Benefits: Early adopters.
    >
    >**Disadvantages of Open-Source OS:**
    >1. Complexity: Hard to set up and maintain.
    >>- Who is Affected: Casual, non-technical users.
    >2. Lack of Official Support: Relies on community help.
    >>- Who is Affected: Businesses needing professional support.
    >3.  Compatibility Issues: May not work with some hardware/software.
    >>- Who is Affected: Users reliant on proprietary tools.
    >4. Security Risks: Vulnerabilities are publicly visible.
    >>- Who is Affected: High-risk environments.
    >5. Fragmentation: Many versions, leading to inconsistency.
    >>- Who is Affected: Users wanting a standardized experience.
