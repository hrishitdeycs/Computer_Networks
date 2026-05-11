In Cisco Packet Tracer, these commands perform an **initial router configuration step-by-step in order**:

1. **`enable`**
   Enters privileged EXEC mode (`Router#`).

2. **`configure terminal`**
   Enters global configuration mode (`Router(config)#`).
   
service password-encryption → Encrypts all plain-text passwords in running config (Type 7 weak encryption).

4. **`hostname cserouter`**
   Changes router name to **cserouter** (prompt becomes `cserouter(config)#`).

5. **`password cse123`**
   Sets a **generic line password**, but on its own it is not applied unless tied to a line (often ignored unless used with specific line config).

6. **`enable secret cse12345`**
   Sets encrypted password for privileged EXEC mode (overrides enable password if both exist).

**`banner motd $Authorized access only$`**
    Displays warning message before login.

7. **`line console 0`**
   Enters console line configuration mode.

8. **`password csexyz`**
   Sets password for console access.

9. **`login`**
   Enforces password authentication on console login.

10. **`exit`**
   Returns to global configuration mode.

11. **`line vty 0 4`**
    Enters VTY (remote access: Telnet/SSH) configuration for 5 lines.

12. **`password csepqr`**
    Sets password for remote access sessions.

13. **`login`**
    Requires password for remote login.

14. **`exit`**
    Returns to global configuration mode.

15. **`exit`**
    Exits to privileged EXEC mode.

16. **`show run`**
    Displays the **running configuration**, showing:

* hostname = cserouter
* enable secret = encrypted (cse12345)
* console password + login enabled
* VTY password + login enabled
* MOTD banner displayed on access
* other default interface/system configs

### Final result

The router becomes secured with:

* Password-protected console access
* Password-protected remote access (Telnet/SSH)
* Encrypted privileged mode password
* Warning banner shown before login
* Custom hostname visible in prompt


<img width="940" height="591" alt="image" src="https://github.com/user-attachments/assets/63236df0-e9f2-4c2f-88df-5777a4e62dfa" />

<img width="681" height="541" alt="image" src="https://github.com/user-attachments/assets/b1092bad-6dac-4c40-a111-4786db43e929" />

<img width="703" height="866" alt="image" src="https://github.com/user-attachments/assets/adb9e58a-64fa-4047-a3bf-8fb6cfd3474e" />

<img width="581" height="730" alt="image" src="https://github.com/user-attachments/assets/ca661212-b680-4bc7-b9de-35ccf635dedd" />

<img width="580" height="884" alt="image" src="https://github.com/user-attachments/assets/2c894716-4945-4880-b1c3-ea9f0344458a" />

We perform **initial router configuration in Cisco Packet Tracer** to prepare the router for basic network operation and management.

### Why it is done:

* To **give the router a unique identity** (hostname)
* To **secure access** (enable passwords, SSH/telnet setup)
* To **prevent unauthorized access**
* To **enable interfaces for communication**
* To **set basic network parameters** so routing works properly

### When it is done:

* **Immediately after adding a new router** in a network
* **Before connecting it to other devices or networks**
* During the **first-time setup in labs or real deployments**
* Before configuring advanced features like routing protocols (OSPF, RIP, etc.)

In short: it’s the **first step after placing a router**, to make it usable, secure, and ready for configuration.

