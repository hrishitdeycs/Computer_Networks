<img width="940" height="394" alt="image" src="https://github.com/user-attachments/assets/1d468489-eb1e-42ca-ab1a-8129cada52d5" />
<img width="940" height="388" alt="image" src="https://github.com/user-attachments/assets/1fe76e9d-e59c-40d0-9e1d-ecdefd831db7" />
In Cisco Packet Tracer, the wire used to connect a PC to a Hub or Switch is:

* **Copper Straight-Through Cable**

### Typical connections using Straight-Through:

* PC ↔ Switch
* PC ↔ Hub
* Router ↔ Switch

### How to select it in Packet Tracer:

1. Click the **Connections** icon (lightning bolt symbol).
2. Choose **Copper Straight-Through**.
3. Click the PC, select **FastEthernet0**.
4. Click the Switch/Hub, select the appropriate port (like FastEthernet0/1).

A quick rule:

* **Different device types** → Straight-through
* **Same device types** (PC ↔ PC, Switch ↔ Switch) → Crossover cable (unless auto-MDIX is enabled).
In Cisco Packet Tracer, a **Star Topology** means all devices connect to a **central device** (Hub or Switch).

### Using a **Hub**

Use a Hub when:

* You want to demonstrate **basic networking concepts**.
* Studying older Ethernet networks.
* Simulating a simple LAN with low traffic.

How it works:

* Hub sends data to **all connected devices**.
* No intelligence or filtering.
* More collisions, slower performance.

Best for:

* Learning/demo purposes only.

Example:
PC1 → Hub ← PC2, PC3

---

### Using a **Switch**

Use a Switch when:

* Building a **modern LAN network**.
* You need better speed and efficiency.
* Simulating real-world enterprise/home networks.

How it works:

* Switch sends data only to the **target device** using MAC addresses.
* Reduces collisions.
* Faster and more secure.

Best for:

* Realistic Packet Tracer labs and practical networking.

Example:
PC1 → Switch ← PC2, PC3

---

### Key Difference

| Feature         | Hub               | Switch                   |
| --------------- | ----------------- | ------------------------ |
| Data forwarding | Broadcasts to all | Sends to specific device |
| Speed           | Slower            | Faster                   |
| Collisions      | More              | Less                     |
| Intelligence    | None              | Uses MAC table           |
| Used today?     | Rarely            | Yes                      |

### In short

* **Hub star topology** → for understanding old/basic networking.
* **Switch star topology** → for real and efficient network design.
