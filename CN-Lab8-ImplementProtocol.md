### ***DNS Server Configuration***
**Domain Name System**

**1. Add Devices:**

* **2 PC-PT**
* **1 Server-PT**
* **1 Switch (2960)** into the workspace.

**2. Connect Devices (Copper Straight-Through):**

* **PC1 → Switch (Fa0/1)**
* **PC2 → Switch (Fa0/2)**
* **Server → Switch (Fa0/24)**

**3. Configure the Server:**

* Click on the **Server** → Go to **Desktop** → **IP Configuration**

  * IP Address: `192.168.1.1`
  * Subnet Mask: `255.255.255.0`
  * Leave Gateway blank (not needed in local DNS)

**4. Enable DNS Service:**

* Go to the **Services** tab → Click on **DNS**

  * Turn **DNS service ON**
  * In the **Name field**, type: `mypage.com`
  * In the **Address field**, type: `192.168.1.1` (same as server IP)
  * Click **Add**

**5. Set Up HTTP Service (Website Content):**

* In the same **Server**, go to **Services** → **HTTP**

  * Scroll to the **HTML section**
  * In **index.html**, type:`<h1>Welcome to mypage.com!</h1>`
  * Click **Save**

**6. Configure the PC:**

* Click on the **PC** **IP Configuration**
  * **PC1** → IP Address: `192.168.1.10`
  * **PC2** → IP Address: `192.168.1.11`
  * Subnet Mask: `255.255.255.0` (same for both pc)
  * **DNS Server:** `192.168.1.1` (same as server IP)

**7. Test the DNS:**

* On the **PC**, open the **Web Browser** from the Desktop tab.
* In the URL bar, type:
  **`mypage.com`** → Press Enter

✅ If configured correctly, the PC should display your HTML page saying **"Welcome to mypage.com!"**

### ***Full DHCP Configuration***
**Dynamic Host Configuration Protocol**
**1. Add Devices:**

* **5 PCs (PC1 to PC5)**
* **1 Server**
* **1 Switch (2960)**

**2. Connect All Devices (Copper Straight-Through):**

* **PC1 → Switch (Fa0/1)**
* **PC2 → Switch (Fa0/2)**
* **PC3 → Switch (Fa0/3)**
* **PC4 → Switch (Fa0/4)**
* **PC5 → Switch (Fa0/5)**
* **Server → Switch (Fa0/24)**

**3. Configure Static IP on Server:**

* Click the **Server** → Go to **Desktop** → **IP Configuration**

  * **IP Address**: `192.168.1.1`
  * **Subnet Mask**: `255.255.255.0`
  * **Default Gateway**: `192.168.1.1`

**4. Enable and Configure DHCP on Server:**

* Go to the **Services** tab → Click **DHCP**

  * Turn **Service** to **ON** and Edit `serverPool`
  * **Pool Name**: `serverPool`
  * **Default Gateway**: `192.168.1.1`
  * **DNS Server**: `192.168.1.1` (or 8.8.8.8)
  * **Starting IP Address**: `192.168.1.10`
  * **Subnet Mask**: `255.255.255.0`
  * **Maximum Number of Users**: `10`
  * Click **Save**

**5. Configure PCs to Receive IP via DHCP:**

For **each PC (PC1 to PC5)**:

* Click on the PC → Go to **Desktop** → Click **IP Configuration**
* Select **DHCP**
* Wait a moment → The PC will automatically receive an IP like:

  * PC1: `192.168.1.10`
  * PC2: `192.168.1.11`
  * PC3: `192.168.1.12`
  * PC4: `192.168.1.13`
  * PC5: `192.168.1.14`

**6. Test the Network:**

* On **any PC**, go to **Desktop** → **Command Prompt**
* Type: `ping 192.168.1.14` (or any other PC’s IP)

✅ If replies are received, DHCP is working and the network is functional.

### ***FTP Server Configuration***
**File Transfer Protocol**
**1. Add Devices:**

* From the bottom-left panel, drag and drop into the workspace:

  * **2 PCs (PC1 and PC2)**
  * **1 Server**
  * **1 Switch (e.g., 2960)**

**2. Connect All Devices (Copper Straight-Through):**

* **PC1 → Switch (Fa0/1)**
* **PC2 → Switch (Fa0/2)**
* **Server → Switch (Fa0/24)**

**3. Configure Static IP on Server:**

* Click **Server** → Go to **Desktop** → **IP Configuration**

  * **IP Address**: `192.168.1.1`
  * **Subnet Mask**: `255.255.255.0`
  * **Default Gateway**: `192.168.1.1`
 
**4. Configure IP on PCs:**

* Go to **Desktop** → **IP Configuration**

  * **PC1 IP**: `192.168.1.10`
  * **PC2 IP**: `192.168.1.11`
  * **Subnet Mask**: `255.255.255.0`
  * **Default Gateway**: `192.168.1.1`

**5. Enable FTP Service and Set User:**

* On **Server**, go to **Services** tab → Select **FTP**

  * Turn **FTP Service** **ON**
  * Under **User Setup**:

    * **Username**: `user1`
    * **Password**: `cn`
    * **Permissions**: Check all boxes (Read, Write, Delete, List, Rename)
    * Click **Add**

**6. Test Network Connectivity:**

* On **PC1**, go to **Command Prompt**

  * Type: `ping 192.168.1.1`
* You should receive replies from the FTP server.

**7. Create a File to FTP Server (PC1)**

* On **PC1**, go to **Desktop** → **Text Editor**
  * Type: `Hello Computer Network`
  * **Ctrl+S** and give file name as **cnfile.txt**

**8. Upload a File to FTP Server (PC1)**

* On **PC1**, go to **Desktop** → **Command Prompt**

  * Type: `ftp 192.168.1.1`
  * Enter username and password
  * `put cnfile.txt` to server
* You should receive replies from the FTP server.

**9. Download File from FTP Server (PC2):**

* On **PC2**, go to **Desktop** → **Command Prompt**

  * Type: `ftp 192.168.1.1`
  * Enter username and password
  * `get cnfile.txt` to server

✅ **You have now successfully shared a file between two PCs using an FTP Server in Packet Tracer.**
