# 📌 Packet Tracer - Network Security Exploration (Physical Mode)

## **🔹 Overview**
This lab explores **network security implementations** in various locations, including a **Data Center, ISP, Coffee Shop, and Home Network** using **Cisco Packet Tracer Physical Mode (PTPM)**. It focuses on **IoT security, VPN configuration, WLAN security, and MAC filtering**.

---

## **📌 Lab Objectives**
### **Part 1: Explore the Networks**
✅ **Investigate different locations**:
- **Data Center:** Network infrastructure, access control lists (ACLs), and IoT security.
- **ISP:** Connectivity between networks.
- **Coffee Shop:** Public Wi-Fi security and VPN setup.
- **Home Network:** WLAN configurations, MAC filtering, and guest network isolation.

### **Part 2: Implement Security Measures**
✅ **Enhance security through configurations**:
- **IoT Smoke Detector Configuration** in the Data Center.
- **VPN Setup on a Laptop** to securely access remote services.
- **Wireless Security Configuration:** WPA2, MAC Filtering, and guest network restrictions.

---

## **📌 Installation & Setup**
### **Requirements:**
1. **Cisco Packet Tracer (Latest Version)**
2. **Packet Tracer Lab File** (`3.11.1-packet-tracer---network-security-exploration---physical-mode.pkt`)
3. **Basic networking knowledge**

### **Steps to Load the Lab**:
1. Open **Cisco Packet Tracer**.
2. Click **File > Open**.
3. Select `3.11.1-packet-tracer---network-security-exploration---physical-mode.pkt`.
4. Start exploring and implementing security configurations.

---

## **📌 Key Features Implemented**
### **🔹 IoT Security**
- Configured an **IoT Smoke Detector** with **WPA2-PSK encryption**.
- Integrated IoT with an authentication server for **remote management**.

### **🔹 VPN Security**
- Configured **VPN on Coffee Shop Laptop** to encrypt internet traffic.
- Verified VPN connection using:
  ```bash
  show crypto isakmp sa
  ```
- Secured **FTP file transfer over VPN**.

### **🔹 Wireless Security (Home Network)**
- **Configured WPA2-PSK for authentication.**
- **Enabled MAC Filtering:** Only **authorized devices** can connect.
- **Created a separate guest network (GuestNet)** that restricts access to local resources.

### **🔹 Access Control & Firewall Rules**
- Implemented **Access Control Lists (ACLs)** to filter network traffic.
- Configured security settings to **block unauthorized access**.

---

## **📌 Directory Structure**
```
📂 Network-Security-Exploration/
 ├── 📁 Documentation/
 │    ├── 3.11.1-packet-tracer---network-security-exploration---physical-mode.pdf
 │    ├── Lab_Report.docx
 │    ├── Network_Topology.png
 │
 ├── 📁 PacketTracer_Files/
 │    ├── 3.11.1-packet-tracer---network-security-exploration---physical-mode.pkt
 │
 ├── 📁 Commands/
 │    ├── Commands-that-will-help.docx
 │
 ├── README.md
```

---

## **📌 How to Run Tests & Validate Configurations**
1. **Test Network Connectivity**
   ```bash
   ping 192.168.0.254   # Check Home Router connectivity
   ping 10.0.0.2        # Check VPN Server connectivity
   ping 8.8.8.8         # Verify external internet access
   ```

2. **Check Active VPN Sessions**
   ```bash
   show crypto isakmp sa
   ```

3. **Verify ACL Rules**
   ```bash
   show access-lists
   ```

4. **Test FTP Transfer Over VPN**
   ```bash
   ftp 172.19.0.3
   get PTsecurity.txt
   ```

---

## **📌 Troubleshooting & Common Issues**
### **❌ Cannot Connect to VPN?**
✔ Ensure correct VPN credentials:
```
GroupName: REMOTE
Group Key: CISCO
Host IP: 10.0.0.2
Username: VPN
Password: ciscorocks
```
✔ Check if VPN tunnel is active:
```
show crypto isakmp sa
```

### **❌ Home Laptop Cannot Connect to HomeNet?**
✔ Verify **MAC Filtering** settings on the router.
✔ Ensure **SSID is correctly entered** in the wireless configuration.

### **❌ Guest Laptop Cannot Access Internet?**
✔ Verify **GuestNet MAC Filtering settings**.
✔ Check **DHCP lease assignment** from the Home Router.

---

## **📌 Real-World Applications & Enhancements**
- **Implement Multi-Factor Authentication (MFA) for VPN Access.**
- **Deploy Next-Generation Firewalls (NGFW) for better security.**
- **Enable Network Intrusion Prevention System (IPS) for advanced threat detection.**
- **Use Biometric Authentication in Data Center for added security.**

---

## **✅ Final Summary**
🚀 Successfully implemented **network security configurations** in **Cisco Packet Tracer**!
- **Applied IoT, VPN, ACLs, WLAN, and MAC Filtering security measures.**
- **Configured secure network segmentation.**
- **Validated VPN access & FTP transfer security.**



