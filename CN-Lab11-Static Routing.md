# Static Routing

1. **Add Devices**

   - Add **two routers** and **two PCs**

2. **Connect the Routers**

   - Select the `GigabitEthernet0/0/0` interface on each router
   - Connect them using a **crossover cable**

3. **Connect PCs to Router0**

   - Select the `FastEthernet0` interface on each PC
   - Connect them to `GigabitEthernet0/0/1` on Router0 using a **straight-through cable**

4. **Configure Router0 Interfaces**

   - `GigabitEthernet0/0/0`:
     - IP Address: `192.168.10.1`
     - Subnet Mask: `255.255.255.0`
   - `GigabitEthernet0/0/1`:
     - IP Address: `192.168.1.1`
     - Subnet Mask: `255.255.255.0`

5. **Configure Router1 Interfaces**

   - `GigabitEthernet0/0/0`:
     - IP Address: `192.168.10.2`
     - Subnet Mask: `255.255.255.0`
   - `GigabitEthernet0/0/1`:
     - IP Address: `192.168.2.1`
     - Subnet Mask: `255.255.255.0`

6. **Configure PC IP Settings**

   - **PC1**:
     - IP Address: `192.168.1.2`
     - Subnet Mask: `255.255.255.0`
     - Default Gateway: `192.168.1.1`
   - **PC2**:
     - IP Address: `192.168.2.2`
     - Subnet Mask: `255.255.255.0`
     - Default Gateway: `192.168.2.1`

7. **Configure Static Routing**

   - On **Router0**, add route:
     - Network: `192.168.2.0`
     - Mask: `255.255.255.0`
     - Next Hop: `192.168.10.2`
   - On **Router1**, add route:
     - Network: `192.168.1.0`
     - Mask: `255.255.255.0`
     - Next Hop: `192.168.10.1`

8. **Test the Network**
   - From **PC1**, run:
     ```bash
     ping 192.168.2.2
     ```
