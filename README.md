# Advanced-Network-Security
Secure Network Design and Implementation project

Overview
This project simulates a secure network environment using tools like GNS3, VMware Workstation, and Kali Linux. Key components include firewalls, VLANs, VPNs, and IDS. The project aims to assess and enhance network security through testing and risk mitigation.

Tools and Technologies
- GNS3: Network emulation
- VMware Workstation: Virtualization
- Kali Linux: Penetration testing tools (Nmap, Wireshark, Hydra)
- Fail2ban: Intrusion detection system
- WatchGuard XTMv: Firewall
- Ubuntu Server: DMZ configuration
<img width="1029" alt="Screenshot 2024-11-30 at 2 17 06 PM" src="https://github.com/user-attachments/assets/8b3c0784-cc4e-4f69-be80-e1df8e64cb41">

Implementation Steps
1. Network Topology Setup
   - Set up the topology in GNS3 with devices imported from VMware and host machines.
   - Components include a WatchGuard Firewall, Layer 3 Switch, Ubuntu Server (DMZ), and Kali Linux (pentesting).

2. Layer 3 Switch and VLAN Configuration
   - Configure VLANs:
     - VLAN 40: ICT Department
     - VLAN 50: Marketing Department
   - Enable IP routing and create DHCP pools for dynamic address allocation.

3. Firewall Setup
   - Configure WatchGuard XTMv interfaces:
     - WAN: Dynamic IP (DHCP)
     - LAN: Bridge interface
     - DMZ: Static IP
   - Set firewall rules to restrict traffic and enable VPN access.

4. VPN Configuration
   - Set up SSL VPN with AES and SHA256 encryption.
   - Test the VPN using a client from the WatchGuard portal and monitor encrypted traffic with Wireshark.

5. Intrusion Detection
   - Install and configure Fail2ban on the DMZ server.
   - Add a custom rule to detect and block SSH brute force attacks.
   - Test the IDS with simulated attacks using Hydra.

6. Security Testing
   - Perform Nmap scans to validate firewall rules and exposed ports.
   - Attempt brute force attacks on the firewall and verify policy enforcement.

7. Risk Assessment and Mitigation
   - Identified Risk: Exposed SSH port (22).
   - Mitigation: Restrict access to required ports and use non-standard ports.

Results
- Firewall blocked unauthorized traffic and malicious scans.
- VPN traffic was encrypted, ensuring secure access.
- Fail2ban successfully detected and blocked SSH brute force attempts.

How to Use
1. Clone this repository:
   git clone <repository-url>
2. Import the GNS3 topology file and deploy virtual machines using VMware.
3. Follow the configuration scripts in the configs/ directory to replicate the setup.
