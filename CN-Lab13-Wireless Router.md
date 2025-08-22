# Wireless Network Setup

## 1. Add Devices

- Add **one Linksys wireless router**
- Add **at least two PCs or laptops**
- Add **one smartphone or tablet**

## 2. Place Devices in Workspace

- Place the **Linksys router** in the center
- Position **PCs/laptops** around the router
- Place the **smartphone/tablet** near the router

## 3. Connect Devices Wirelessly

- No cables are needed — devices will connect using **wireless signals**

## 4. Configure the Wireless Router

- Click on the router → go to **Config** tab
- Under **Wireless**, set:
  - **SSID**: `MyHomeNetwork`
  - **Channel**: `6`
  - **Security Mode**: `WPA2-PSK`
  - **Pre-shared Key**: `password123`
- (Optional) Under **GUI** tab:
  - Internet IP: **DHCP** (or Static if required)
  - Local IP: `192.168.0.1`
  - Subnet Mask: `255.255.255.0`
  - Enable **DHCP Server**

## 5. Connect PCs/Laptops to Wi-Fi

- Click a PC/laptop → go to **Desktop tab**
- Open **PC Wireless** (for PCs) or **Laptop Wireless** (for laptops)
- Click **Connect**
- Choose the wireless network: `MyHomeNetwork`
- Enter password: `password123`

## 6. Connect Smartphone/Tablet

- Open **Wireless Settings** on the device
- Select `MyHomeNetwork`
- Enter the password: `password123`

## 7. Test the Network

- On one device, open **Command Prompt**
- Type:
  ```bash
  ping 192.168.0.X
  ```
