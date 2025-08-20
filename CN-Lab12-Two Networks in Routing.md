1. Add two routers and four PCs.
2. Add two switches.
3. Connect Router1 to Switch1:
   • Use a copper straight-through cable.
   • Connect FastEthernet0/0 on Router1 to FastEthernet0/1 on Switch1.
4. Connect Router2 to Switch2:
   • Use a copper straight-through cable.
   • Connect FastEthernet0/0 on Router2 to FastEthernet0/1 on Switch2.
5. Connect two PCs to Switch1:
   • PC1 to FastEthernet0/2
   • PC2 to FastEthernet0/3
6. Connect two PCs to Switch2:
   • PC3 to FastEthernet0/2
   • PC4 to FastEthernet0/3
7. Connect Router1 to Router2:
   • Use a crossover cable.
   • Connect FastEthernet0/1 on Router1 to FastEthernet0/1 on Router2.
8. Assign IP addresses on Router1:
   • FastEthernet0/0: IP = 192.168.10.1, Subnet Mask = 255.255.255.0
   • FastEthernet0/1: IP = 192.168.30.1, Subnet Mask = 255.255.255.252
9. Assign IP addresses on Router2: 
   • FastEthernet0/0: IP = 192.168.20.1, Subnet Mask = 255.255.255.0
   • FastEthernet0/1: IP = 192.168.30.2, Subnet Mask = 255.255.255.252
10. Assign IP addresses
   • PC1: IP = 192.168.10.2, Mask = 255.255.255.0, Gateway = 192.168.10.1
   • PC2: IP = 192.168.10.3, Mask = 255.255.255.0, Gateway = 192.168.10.1
   • PC3: IP = 192.168.20.2, Mask = 255.255.255.0, Gateway = 192.168.20.1
   • PC4: IP = 192.168.20.3, Mask = 255.255.255.0, Gateway = 192.168.20.1
11. Configure static route on Router1:
   • Network: 192.168.20.0
   • Mask: 255.255.255.0
   • Next-Hop: 192.168.30.2
12. Configure static route on Router2:
   • Network: 192.168.10.0
   • Mask: 255.255.255.0
   • Next-Hop: 192.168.30.1
13. Test the Network
   • Open PC1 → Command Prompt → Type: ping 192.168.20.21. Add two routers and four PCs.
2. Add two switches.
3. Connect Router1 to Switch1:
   • Use a copper straight-through cable.
   • Connect FastEthernet0/0 on Router1 to FastEthernet0/1 on Switch1.
4. Connect Router2 to Switch2:
   • Use a copper straight-through cable.
   • Connect FastEthernet0/0 on Router2 to FastEthernet0/1 on Switch2.
5. Connect two PCs to Switch1:
   • PC1 to FastEthernet0/2
   • PC2 to FastEthernet0/3
6. Connect two PCs to Switch2:
   • PC3 to FastEthernet0/2
   • PC4 to FastEthernet0/3
7. Connect Router1 to Router2:
   • Use a crossover cable.
   • Connect FastEthernet0/1 on Router1 to FastEthernet0/1 on Router2.
8. Assign IP addresses on Router1:
   • FastEthernet0/0: IP = 192.168.10.1, Subnet Mask = 255.255.255.0
   • FastEthernet0/1: IP = 192.168.30.1, Subnet Mask = 255.255.255.252
9. Assign IP addresses on Router2: 
   • FastEthernet0/0: IP = 192.168.20.1, Subnet Mask = 255.255.255.0
   • FastEthernet0/1: IP = 192.168.30.2, Subnet Mask = 255.255.255.252
10. Assign IP addresses
   • PC1: IP = 192.168.10.2, Mask = 255.255.255.0, Gateway = 192.168.10.1
   • PC2: IP = 192.168.10.3, Mask = 255.255.255.0, Gateway = 192.168.10.1
   • PC3: IP = 192.168.20.2, Mask = 255.255.255.0, Gateway = 192.168.20.1
   • PC4: IP = 192.168.20.3, Mask = 255.255.255.0, Gateway = 192.168.20.1
11. Configure static route on Router1:
   • Network: 192.168.20.0
   • Mask: 255.255.255.0
   • Next-Hop: 192.168.30.2
12. Configure static route on Router2:
   • Network: 192.168.10.0
   • Mask: 255.255.255.0
   • Next-Hop: 192.168.30.1
13. Test the Network
   • Open PC1 → Command Prompt → Type: ping 192.168.20.2
