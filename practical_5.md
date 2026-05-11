Here is what happens **line by line in Cisco Packet Tracer (initial switch configuration)**:

* **enable** → Moves from user EXEC mode to privileged EXEC mode (`Switch#`).
* **configure terminal** → Enters global configuration mode (`Switch(config)#`).
* **service password-encryption** → Encrypts all plain-text passwords in running config (Type 7 weak encryption).
* **enable password cse123** → Sets a fallback privileged mode password (but will be ignored if enable secret is present).
* **enable secret cse12345** → Sets the main encrypted password for privileged EXEC mode (this overrides `enable password`).
* **banner motd # Unauthorized access prohibited #** → Displays warning message to anyone accessing the device.
* **line console 0** → Enters console line configuration mode.

  * **password csexyz** → Sets console login password.
  * **login** → Forces users to enter the console password.
* **exit** → Returns to global configuration mode.
* **line vty 0 15** → Enters VTY (remote Telnet/SSH) line configuration mode.

  * **password csepqr** → Sets password for remote access.
  * **login** → Requires password for VTY access.
* **exit** → Returns to global configuration mode.
* **exit** → Leaves configuration mode and returns to privileged EXEC mode.
* **show running-config** → Displays the current active configuration (you will see encrypted passwords and all applied settings).

**Overall result:**
The switch becomes secured with encrypted passwords, console and remote access protection, an MOTD warning banner, and a protected enable (privileged) mode using `cse12345` as the effective password.

In Cisco Packet Tracer (IOS), these commands set up basic switch configuration in sequence:

* **`enable`**
  Switches from **user EXEC mode** (`>`) to **privileged EXEC mode** (`#`), giving access to configuration commands.

* **`configure terminal`** (or `conf t`)
  Enters **global configuration mode**, where you can change device settings.

* **`hostname cseswitch`**
  Sets the switch’s **device name** to `cseswitch`, which replaces the default name (e.g., `Switch`) in the CLI prompt.

So after running them in order, the prompt changes like:
`Switch>` → `Switch#` → `Switch(config)#` → `cseswitch(config)#`

<img width="940" height="556" alt="image" src="https://github.com/user-attachments/assets/b8803cfc-dd37-4643-99cf-2b7b8eb699fc" />


**`enable password cse123`**

in Cisco Packet Tracer (global configuration mode), it:

* Sets the **privileged EXEC mode password** to `cse123`.
* This means when someone types **`enable`** from user EXEC mode, they will be prompted to enter this password to access `#` mode.

 Important note:

* This password is stored in **plain text (unencrypted)** in the running configuration.
* A better practice is to use:
  **`enable secret cse123`** → this stores the password in **encrypted form** and overrides `enable password` if both are set.

So in short:
 `enable password cse123` protects access to privileged mode using that password, but it is not secure compared to `enable secret`.


<img width="706" height="583" alt="image" src="https://github.com/user-attachments/assets/9ffe829d-5f6a-4c3b-a6a8-f1e9c8b5cdc8" />

<img width="744" height="613" alt="image" src="https://github.com/user-attachments/assets/151f05f0-93dd-45f3-8809-c4bf37f137a8" />

In Cisco Packet Tracer, during initial switch configuration, these commands are used to secure console access:

* `line console 0` → enters **console line configuration mode** (for direct physical console access to the switch).
* `password csexyz` → sets the **password “csexyz”** for console access.
* `login` → tells the switch to **require that password** when someone tries to access the console.

### In order, their effect:

They configure the switch so that anyone connecting through the console port must enter the password **csexyz** before gaining access.

Without `login`, the password is ignored; the system would not prompt for it.


<img width="775" height="670" alt="image" src="https://github.com/user-attachments/assets/c019f6d3-dd24-41e5-b8bd-83de8a224977" />

In Cisco Packet Tracer, under global configuration mode for an initial switch setup, these commands configure remote access (Telnet/SSH line settings):

* **`line vty 0 15`**
  Enters configuration mode for the virtual terminal (VTY) lines 0 through 15. These lines control remote access sessions to the device.

* **`password csepqr`**
  Sets the password **"csepqr"** for those VTY lines. Anyone attempting remote access must provide this password.

* **`login`**
  Enables password checking on those VTY lines. Without this, the password you set would not be enforced.

### In short:

Together, they configure the switch to allow remote access (like Telnet/SSH) and require the password **csepqr** before granting login access.


<img width="766" height="742" alt="image" src="https://github.com/user-attachments/assets/4bb3d9ff-a186-4fe3-9c1b-b1f36349e707" />

In Cisco Packet Tracer (privileged EXEC mode), the command:

**`show running-config` (or `sh run`)**

displays the **current active configuration** stored in the device’s RAM.

### What it does during initial switch configuration:

* Shows all **live settings** currently applied (e.g., VLANs, interfaces, passwords, IP settings).
* Lets you verify what has been configured so far.
* Reflects **changes immediately**, even before saving.

### Key point:

It shows the **running (active) config**, not the saved startup config (which is in NVRAM).



<img width="749" height="867" alt="image" src="https://github.com/user-attachments/assets/6ded591f-32f6-470f-985b-6ef9c29702ef" />

<img width="709" height="884" alt="image" src="https://github.com/user-attachments/assets/2fb2e23e-4889-4599-862b-e1a57684329a" />

<img width="548" height="536" alt="image" src="https://github.com/user-attachments/assets/eddd8ce9-8813-4b27-ade0-bbc0349dfc5b" />

In Cisco Packet Tracer, when you configure those two commands in global configuration mode, they do different things:

### 1. `banner motd $***Only Authorized users allowed***$`

* Sets a **Message of the Day (MOTD) banner**.
* This message is displayed **immediately when someone connects to the switch (console, SSH, Telnet)**, before login.
* Purpose: **Security warning / legal notice / access restriction message**.
* The `$` is just the delimiter defining the start and end of the message (you could use other symbols like `#`, `@`, etc.).

 Result: Anyone accessing the device sees:
**Only Authorized users allowed**

---

### 2. `service password-encryption`

* Encrypts all **plain-text passwords** stored in the configuration file (e.g., console, VTY, enable passwords).
* Uses a **weak Type 7 encryption** (not secure for real security, but hides passwords from casual viewing).
* Purpose: Prevents passwords from being visible in plain text in `show running-config`.

 Result: Passwords appear scrambled instead of readable.

---

### In short:

* **banner motd** → Shows a warning message before login.
* **service password-encryption** → Hides stored passwords in configuration output (basic obfuscation).


### Why we perform initial switch configuration

We do it to make a Cisco switch usable, secure, and manageable instead of leaving it in default (unsecured) state. By default, a switch has no password protection, no hostname, and no remote management setup.

### When we do it

We perform initial configuration:

* **Immediately after placing a new switch in a network (Packet Tracer or real device)**
* **Before connecting it to other network devices**
* **Before allowing user traffic or remote access**

### What it typically includes (basic idea)

* Setting a **hostname**
* Configuring **enable/console/VTY passwords**
* Disabling unused ports (sometimes)
* Assigning a **management IP (VLAN 1 or management VLAN)**
* Saving configuration

### In short

We do it at the start to secure and prepare the switch so it can be safely used and managed in a network.
