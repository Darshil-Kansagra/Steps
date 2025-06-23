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
