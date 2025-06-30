***Bus***

### **1. Add Devices:**

* Drag and drop **4 PCs**: `PC1`, `PC2`, `PC3`, `PC4`.
* Drag and drop **4 Switches**: `Switch1`, `Switch2`, `Switch3`, `Switch4`.

### **2. Connect PCs to Switches (Straight-Through Cable):**

* Click **Connections (lightning bolt icon)** → Select **Copper Straight-Through**.
* Connect:

  * **PC1 → Switch1 (FastEthernet0/1)**
  * **PC2 → Switch2 (FastEthernet0/1)**
  * **PC3 → Switch3 (FastEthernet0/1)**
  * **PC4 → Switch4 (FastEthernet0/1)**

### **3. Connect Switches Together (Crossover Cable):**

* Select **Copper Cross-over** cable.
* Connect:

  * **Switch1 (Fa0/24) ↔ Switch2 (Fa0/24)**
  * **Switch2 (Fa0/23) ↔ Switch3 (Fa0/23)**
  * **Switch3 (Fa0/22) ↔ Switch4 (Fa0/22)**

### **4. Assign IP Addresses to All PCs:**

Go to each PC → **Desktop** tab → **IP Configuration**, and enter:

* **PC1:**

  * IP: `192.168.1.1`
  * Subnet Mask: `255.255.255.0`

* **PC2:**

  * IP: `192.168.1.2`
  * Subnet Mask: `255.255.255.0`

* **PC3:**

  * IP: `192.168.1.3`
  * Subnet Mask: `255.255.255.0`

* **PC4:**

  * IP: `192.168.1.4`
  * Subnet Mask: `255.255.255.0`

### **5. Test the Network:**

* Open **Command Prompt** on any PC
  ping 192.168.1.4
