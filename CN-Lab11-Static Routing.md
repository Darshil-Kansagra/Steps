1. Add two router and two pc
2. Connect the Routers: Router, and select the GigabitEthernet 0/0/0 interface. With other router cross-over cable
3. Both pc to router, select the FastEthernet0 interface, and connect it to GigabitEthernet 0/0/1 on Router0 with straightthrough
4. Go to config tab and GigabitEthernet 0/0/0 under INTERFACE. Set the IP Address to 192.168.10.1 and the Subnet Mask to 255.255.255.0
5. Go to config tab GigabitEthernet 0/0/1 and set the IP Address to 192.168.1.1 with the Subnet Mask as 255.255.255.0
6. Click on GigabitEthernet 0/0/0 under INTERFACE. Set the IP Address to 192.168.10.2 and the Subnet Mask to 255.255.255.0 for other route
7. Click on GigabitEthernet 0/0/1 and set the IP Address to 192.168.2.1 with the Subnet Mask as 255.255.255.0 for other router.
8. Set ip address to first pc 192.168.1.2 and default gateway to 192.168.1.1
9. Set ip address to first pc 192.168.2.2 and default gateway to 192.168.2.1
10. Under ROUTING, select Static. Click Add, and enter the following: Network: 192.168.2.0 Mask: 255.255.255.0 NextHop: 192.168.10.2
11. Under ROUTING, select Static. Click Add, and enter the following: Network: 192.168.1.0 Mask: 255.255.255.0 NextHop: 192.168.10.1
12. Test the network using ping 192.168.2.2
