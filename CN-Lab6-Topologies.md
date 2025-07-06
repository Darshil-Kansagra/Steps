### ***Tree***

**1. Add Devices:**

From the bottom-left panel, drag and drop **four PC-PT devices** into the workspace. Then, drag and drop **three 2960 switches** into the workspace.

**2. Connect the PCs (Copper Straight-Through):**

* **PC1 → Switch2 (FastEthernet0/1)**
* **PC2 → Switch2 (FastEthernet0/2)**
* **PC3 → Switch3 (FastEthernet0/1)**
* **PC4 → Switch3 (FastEthernet0/2)**

**3. Connect the Switches (Copper Cross-over):**

* **Switch1 (FastEthernet0/24) ↔ Switch2 (FastEthernet0/24)**
* **Switch1 (FastEthernet0/23) ↔ Switch3 (FastEthernet0/23)**

### **4. Configure IP Addresses:**

Set the following IP addresses and subnet mask for each PC:

* **PC1:** IP Address: `192.168.0.1`
* **PC2:** IP Address: `192.168.0.2`
* **PC3:** IP Address: `192.168.0.3`
* **PC4:** IP Address: `192.168.0.4`
* **Subnet Mask:** `255.255.255.0` (same for all)

**5. Test the Network:**

Open **Command Prompt** on any PC , and type:`192.168.0.3`

### ***Mesh***
**1. Add Devices:**

From the bottom-left panel, drag and drop **four PC-PT devices** and **four 2960 switches** into the workspace.

**2. Connect the PCs (Copper Straight-Through):**

* **PC1 → Switch1 (FastEthernet0/1)**
* **PC2 → Switch2 (FastEthernet0/1)**
* **PC3 → Switch3 (FastEthernet0/1)**
* **PC4 → Switch4 (FastEthernet0/1)**

**3. Connect the Switches (Copper Cross-over):**

* **Switch1(FastEthernet0/24) ↔ Switch2(FastEthernet0/24)**
* **Switch1(FastEthernet0/23) ↔ Switch3(FastEthernet0/23)**
* **Switch1(FastEthernet0/22) ↔ Switch4(FastEthernet0/22)**
* **Switch2(FastEthernet0/21) ↔ Switch3(FastEthernet0/21)**
* **Switch2(FastEthernet0/20) ↔ Switch4(FastEthernet0/20)**
* **Switch3(FastEthernet0/19) ↔ Switch4(FastEthernet0/19)**

**4. Configure IP Addresses:**

* **PC1:** 192.168.0.1
* **PC2:** 192.168.0.2
* **PC3:** 192.168.0.3
* **PC4:** 192.168.0.4
* **Subnet Mask:** 255.255.255.0 (same for all)

### **5. Test the Network:**

Open **Command Prompt** on any PC and type: `192.168.0.2`
