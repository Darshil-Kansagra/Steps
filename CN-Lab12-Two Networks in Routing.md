# Two Networks in Routing

1. **Add Devices**

   - Add **two routers** and **four PCs**
   - Add **two switches**

2. **Connect Router1 to Switch1**

   - Use a **copper straight-through** cable
   - Connect `FastEthernet0/0` on **Router1** to `FastEthernet0/1` on **Switch1**

3. **Connect Router2 to Switch2**

   - Use a **copper straight-through** cable
   - Connect `FastEthernet0/0` on **Router2** to `FastEthernet0/1` on **Switch2**

4. **Connect PCs to Switch1**

   - **PC1** → `FastEthernet0/2`
   - **PC2** → `FastEthernet0/3`

5. **Connect PCs to Switch2**

   - **PC3** → `FastEthernet0/2`
   - **PC4** → `FastEthernet0/3`

6. **Connect Router1 to Router2**

   - Use a **crossover cable**
   - Connect `FastEthernet0/1` on **Router1** to `FastEthernet0/1` on **Router2**

7. **Assign IP Addresses on Router1**

   - `FastEthernet0/0`: **192.168.10.1 / 255.255.255.0**
   - `FastEthernet0/1`: **192.168.30.1 / 255.255.255.252**

8. **Assign IP Addresses on Router2**

   - `FastEthernet0/0`: **192.168.20.1 / 255.255.255.0**
   - `FastEthernet0/1`: **192.168.30.2 / 255.255.255.252**

9. **Assign IP Addresses on PCs**

   - **PC1**: IP = `192.168.10.2`, Mask = `255.255.255.0`, Gateway = `192.168.10.1`
   - **PC2**: IP = `192.168.10.3`, Mask = `255.255.255.0`, Gateway = `192.168.10.1`
   - **PC3**: IP = `192.168.20.2`, Mask = `255.255.255.0`, Gateway = `192.168.20.1`
   - **PC4**: IP = `192.168.20.3`, Mask = `255.255.255.0`, Gateway = `192.168.20.1`

10. **Configure Static Route on Router1**

    - Network: `192.168.20.0`
    - Mask: `255.255.255.0`
    - Next-Hop: `192.168.30.2`

11. **Configure Static Route on Router2**

    - Network: `192.168.10.0`
    - Mask: `255.255.255.0`
    - Next-Hop: `192.168.30.1`

12. **Test the Network**
    - On **PC1** → Open **Command Prompt**
    - Type:
      ```bash
      ping 192.168.20.2
      ```
