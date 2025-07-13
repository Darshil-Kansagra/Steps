### ✅ VLAN Setup (Admin, HR, Employee)

**1. Add Devices**

  * **5 PC-PT** (PC1 to PC5)
  * **4 Laptop-PT** (Laptop1 to Laptop4)
  * **2 Switches (2960)**

**2. Connect Devices (Copper Straight-Through)**

**Switch1 Connections**

* PC1 → Fa0/1
* PC2 → Fa0/2
* PC3 → Fa0/3
* PC4 → Fa0/4
* PC5 → Fa0/5

**Switch2 Connections**

* Laptop1 → Fa0/1
* Laptop2 → Fa0/2
* Laptop3 → Fa0/3
* Laptop4 → Fa0/4

**3. Connect Switches (Copper Cross-Over)**

* **Switch1 Fa0/24** ↔ **Switch2 Fa0/24**

**4. Assign IP Addresses**

Go to **each device → Desktop → IP Configuration**
Set IP Address and Subnet Mask (`255.255.255.0` for all):

| Device  | IP Address   | VLAN     |
| ------- | ------------ | -------- |
| PC1     | 192.168.10.1 | Admin    |
| PC2     | 192.168.10.2 | Admin    |
| PC3     | 192.168.20.1 | HR       |
| PC4     | 192.168.20.2 | HR       |
| PC5     | 192.168.20.3 | HR       |
| Laptop1 | 192.168.40.1 | Employee |
| Laptop2 | 192.168.40.2 | Employee |
| Laptop3 | 192.168.40.3 | Employee |
| Laptop4 | 192.168.40.4 | Employee |

**5. Create VLANs on Each Switch(Both Switch)**

> Switch → **Config tab → VLAN Database**

Create:

| VLAN ID  | Name     |
| -------- | -------- |
| 100      | Admin    |
| 200      | HR       |
| 300      | Employee |

**6. Assign VLANs to Interfaces**

> Switch → **Config tab → Interface → Select Port → Set Mode: Access → Choose VLAN**

**Switch1 VLAN Assignment**

| Port  | Device | VLAN  |
| ----- | ------ | ----- |
| Fa0/1 | PC1    | Admin |
| Fa0/2 | PC2    | Admin |
| Fa0/3 | PC3    | HR    |
| Fa0/4 | PC4    | HR    |
| Fa0/5 | PC5    | HR    |

**Switch2 VLAN Assignment**

| Port  | Device  | VLAN     |
| ----- | ------- | -------- |
| Fa0/1 | Laptop1 | Employee |
| Fa0/2 | Laptop2 | Employee |
| Fa0/3 | Laptop3 | Employee |
| Fa0/4 | Laptop4 | Employee |

**7. Set Trunk Port**

> On both Switches → Interface Fa0/24
> Set **Mode: Trunk**

**8. Test Connectivity**

> From any device, go to **Desktop → Command Prompt**

* ✅ `ping` between same VLAN IPs should work
  Example: `ping 192.168.10.2` from PC1
* ❌ `ping` across VLANs will **fail**
