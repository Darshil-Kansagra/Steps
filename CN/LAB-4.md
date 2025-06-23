***Point-To-Point***

1. Add Two PCs**: From the bottom-left panel, drag and drop two **PC-PT** devices into the workspace.

2. **Connect the PCs**:

   * Click the **Connections (lightning bolt)** icon.
   * Select **Copper Straight-Through** cable.
   * Click **PC1 → FastEthernet0**, then **PC2 → FastEthernet0**.

3. **Assign IP Addresses**:

   * Click on **PC1**, go to the **Desktop** tab → click **IP Configuration**.
     Set IP: `192.168.0.1`, Subnet Mask: `255.255.255.0`.
   * Do the same on **PC2**, but use IP: `192.168.0.2`.

4. **Test the Connection**:

   * On **PC1**, open **Command Prompt** (Desktop tab).
   * Type `ping 192.168.0.2` and press Enter.
  
***Client-Server***  

1. **Add Devices**:

   * Drag and drop **one Server (Server-PT)**, **two PCs (PC-PT)**, and **one Switch (Switch-PT)** into the workspace.

2. **Connect the Devices**:

   * Use **Copper Straight-Through** cables:

     * **PC1 → Switch FastEthernet0/1**
     * **PC2 → Switch FastEthernet0/2**
     * **Server → Switch FastEthernet0/3**

3. **Assign IP Addresses**:

   * **PC1**: `192.168.0.3` / `255.255.255.0`
   * **PC2**: `192.168.0.4` / `255.255.255.0`
   * **Server**: `192.168.0.5` / `255.255.255.0`

4. **Enable Server Service**:

   * Click the **Server**, go to the **Services** tab.
   * Enable a service like **HTTP** or **FTP**.

5. **Test the Setup**:

   * On **PC1**, go to **Desktop → Web Browser**.
   * Enter: `http://192.168.0.5`
