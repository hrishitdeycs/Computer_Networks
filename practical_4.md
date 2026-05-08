# Bus topology
<img width="833" height="483" alt="image" src="https://github.com/user-attachments/assets/1a7a6f9b-a062-42fe-8ad4-6565ac2beba0" />
<img width="940" height="792" alt="image" src="https://github.com/user-attachments/assets/7737ecd5-a66f-43a2-acc9-f92c7783338d" />
<img width="686" height="602" alt="image" src="https://github.com/user-attachments/assets/ab2c0fdd-ccd2-42c4-9d94-583d1582e25c" />
A bus topology connects all devices to a single shared cable (the “bus”). In Cisco Packet Tracer, it’s mostly used for learning basic networking concepts, not modern real-world deployments.

### Why use bus topology?

* **Simple and cheap** — fewer cables and devices needed.
* **Easy to understand** for beginners studying networking.
* Demonstrates concepts like:

  * shared communication medium
  * collisions
  * broadcast traffic
  * terminators in older Ethernet networks

### When do we use it in Packet Tracer?

Use it when:

* practicing **network topology types** for exams/classes
* simulating **legacy Ethernet networks**
* comparing bus vs star/ring topologies
* learning how data travels on a shared line

### Important note

In real modern networks, **star topology** is preferred because it is:

* faster
* more reliable
* easier to troubleshoot

Bus topology is now mostly **educational or historical**.
# Ring topology
<img width="756" height="572" alt="image" src="https://github.com/user-attachments/assets/2972c202-1964-442f-ae42-8a501a1c72d7" />
<img width="940" height="776" alt="image" src="https://github.com/user-attachments/assets/5b83df65-7fdb-4f9f-b4d9-ec83deb9052d" />
<img width="763" height="536" alt="image" src="https://github.com/user-attachments/assets/bc3727e0-7de9-4918-8d52-576b84bd8841" />
A **ring topology** connects each device to **two neighboring devices**, forming a closed loop.

In Cisco Packet Tracer, you usually use ring topology for:

* **Learning network concepts** — especially token passing, redundancy, and path loops.
* **Studying redundancy/failover** — if one link fails, traffic can travel the opposite direction (in dual-ring setups).
* **Understanding protocols like STP** (Spanning Tree Protocol), which prevents switching loops in rings.
* **Simulating MAN/WAN networks** where providers often use ring designs for reliability.
* **Testing fault tolerance** in labs and CCNA practice.

### Why use it?

* Better **reliability** than a simple line topology.
* Can provide **backup paths**.
* Useful for demonstrating **network loop behavior** and prevention.

### When is it used?

* In **educational labs** and certification practice.
* In some **metro fiber networks** and industrial systems.
* When you need **high availability** with alternate paths.

### Drawback

* More complex than star topology.
* Without proper protocols, rings can create **broadcast storms/loops**.

In real modern LANs, **star topology** is far more common, but ring topology is still important for understanding networking fundamentals.
# Tree topology
<img width="940" height="381" alt="image" src="https://github.com/user-attachments/assets/2a30ac67-1bdd-49d3-9757-0f6281ae8fb8" />
<img width="940" height="776" alt="image" src="https://github.com/user-attachments/assets/01200ca7-f5fd-4c83-9e50-b811612c7fb9" />
<img width="792" height="572" alt="image" src="https://github.com/user-attachments/assets/ad013a9e-9e4d-4217-abb3-44e4ad2a20fe" />

In Cisco Packet Tracer, we use a **tree topology** when we need a **hierarchical network structure** that combines multiple star networks in a scalable way.

### **Why we use tree topology**

* **Scalability:** Easy to expand by adding branches (new switches/sub-networks)
* **Organization:** Groups devices in layers (core → distribution → access)
* **Efficient management:** Easier troubleshooting and control compared to flat networks
* **Reduced congestion:** Segments traffic into different branches

### **When we use it**

* Large networks like **campuses, schools, or enterprises**
* When multiple departments or floors need separate LANs
* When a **central backbone (root/core switch)** connects multiple star networks
* In Packet Tracer labs demonstrating **hierarchical network design**

### **In short**

We use tree topology in Packet Tracer when we need a **large, structured, and expandable network with layered control and multiple connected LANs**.
