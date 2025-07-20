### ***DNS Server Configuration***

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
  * **PC1** → IP Address: `192.168.2.1`
  * **PC2** → IP Address: `192.168.2.2`
  * Subnet Mask: `255.255.255.0` (same for both pc)
  * **DNS Server:** `192.168.1.1` (same as server IP)

**7. Test the DNS:**

* On the **PC**, open the **Web Browser** from the Desktop tab.
* In the URL bar, type:
  **`mypage.com`** → Press Enter

✅ If configured correctly, the PC should display your HTML page saying **"Welcome to mypage.com!"**
