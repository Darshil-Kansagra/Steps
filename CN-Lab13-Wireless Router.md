1. Add Devices:
    • Add one Linksys wireless router.
    • Add at least two PCs or laptops.
    • Add one smartphone or tablet.
2. Place Devices in Workspace:
    • Place the Linksys router in the center.
    • Position PCs/laptops around the router.
    • Place the smartphone/tablet near the router.
3. Connect Devices Wirelessly:
    • No cables needed — devices will use wireless connections.
4. Configure the Wireless Router:
    • Click the router → go to Config tab.
    • Under Wireless, set:
        o SSID: MyHomeNetwork
        o Channel: 6
        o Security Mode: WPA2-PSK
        o Pre-shared Key: password123
    • (Optional) Under GUI tab, set:
        o Internet IP: DHCP (or Static if needed)
        o Local IP: 192.168.0.1, Mask: 255.255.255.0
        o Enable DHCP Server
5. Connect PCs/Laptops to Wi-Fi:
    • Click a PC/laptop → go to Desktop tab
    • Open PC Wireless or Laptop Wireless
    • Click Connect → choose MyHomeNetwork
    • Enter password: password123
6. Connect Smartphone/Tablet:
    • Open Wireless Settings on device
    • Connect to MyHomeNetwork with password password123
7. Test the Network:
    • On one device, open Command Prompt
    • Type: ping 192.168.0.X (replace X with the other device’s IP)