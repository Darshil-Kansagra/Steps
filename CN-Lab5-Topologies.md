### ***Bus***

**1. Add Devices:**

* Drag and drop **4 PCs**: `PC1`, `PC2`, `PC3`, `PC4`.
* Drag and drop **4 Switches**: `Switch1`, `Switch2`, `Switch3`, `Switch4`.

**2. Connect PCs to Switches (Straight-Through Cable):**

* Connect:

  * **PC1 → Switch1 (FastEthernet0/1)**
  * **PC2 → Switch2 (FastEthernet0/1)**
  * **PC3 → Switch3 (FastEthernet0/1)**
  * **PC4 → Switch4 (FastEthernet0/1)**

**3. Connect Switches Together (Crossover Cable):**

* Connect:

  * **Switch1 (Fa0/24) ↔ Switch2 (Fa0/24)**
  * **Switch2 (Fa0/23) ↔ Switch3 (Fa0/23)**
  * **Switch3 (Fa0/22) ↔ Switch4 (Fa0/22)**

**4. Assign IP Addresses to All PCs:**

Go to each PC → **Desktop** tab → **IP Configuration**, and enter:

* **PC1:** `192.168.1.1`/`255.255.255.0`

* **PC2:**
`192.168.1.2`/`255.255.255.0`

* **PC3:**
`192.168.1.3`/`255.255.255.0`

* **PC4:**
`192.168.1.4`/`255.255.255.0`

**5. Test the Network:**

* Open **Command Prompt** on any PC
  ping 192.168.1.4

### ***Star***

**1. Add Devices:**

* Drag and drop **5 PCs**: `PC1`, `PC2`, `PC3`, `PC4`,`PC5`.
* Drag and drop **1 Switches**: `Switch1`.

**2. Connect PCs to Switches (Straight-Through Cable):**

* Connect:

  * **PC1 → Switch1 (FastEthernet0/1)**
  * **PC2 → Switch1 (FastEthernet0/2)**
  * **PC3 → Switch1 (FastEthernet0/3)**
  * **PC4 → Switch1 (FastEthernet0/4)**
  * **PC5 → Switch1 (FastEthernet0/5)**

**3. Assign IP Addresses to All PCs:**

Go to each PC → **Desktop** tab → **IP Configuration**, and enter:

* **PC1:** `192.168.1.1`/`255.255.255.0`

* **PC2:**
`192.168.1.2`/`255.255.255.0`

* **PC3:**
`192.168.1.3`/`255.255.255.0`

* **PC4:**
`192.168.1.4`/`255.255.255.0`

* **PC5:**
`192.168.1.5`/`255.255.255.0`

**4. Test the Network:**

* Open **Command Prompt** on any PC
  ping 192.168.1.4

### ***Ring***

**1. Add Devices:**

From the **bottom-left panel**, drag and drop **four PC-PT devices** into the workspace.
Then, drag and drop **four 2960 switches** into the workspace.

**2. Connect the PCs:(Copper Straight-Through)**

  * **PC1 → Switch1 (FastEthernet0/1)**
  * **PC2 → Switch2 (FastEthernet0/1)**
  * **PC3 → Switch3 (FastEthernet0/1)**
  * **PC4 → Switch4 (FastEthernet0/1)**

**3. Connect the Switches:(Copper Cross-over)**

  * **Switch1 (FastEthernet0/24) ↔ Switch2 (FastEthernet0/24)**
  * **Switch2 (FastEthernet0/23) ↔ Switch3 (FastEthernet0/23)**
  * **Switch3 (FastEthernet0/22) ↔ Switch4 (FastEthernet0/22)**
  * **Switch4 (FastEthernet0/21) ↔ Switch1 (FastEthernet0/20)**

**4. Configure IP Addresses:**

* **PC1**: IP Address: `192.168.0.1`

* **PC2**: IP Address: `192.168.0.2`

* **PC3**: IP Address: `192.168.0.3`

* **PC4**: IP Address: `192.168.0.4`

* **Subnet Mask:** `255.255.255.0` (same for all)

**5. Test the Network:**

* Open **Command Prompt** on any PC
  ping 192.168.0.4
