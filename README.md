# Capture and Analyze Network Traffic Using Wireshark

## 🎯 Objective
Capture live network packets and identify basic protocols and traffic types using Wireshark.

---

## 🛠 Tools Used
- **Wireshark** (Network protocol analyzer)
- **Kali Linux** (Running on VirtualBox)
- **Websites Accessed**:
  - [nfsu.ac.in](https://nfsu.ac.in)
  - [w3schools.com](https://www.w3schools.com)
  - [google.com](https://www.google.com)

---

## 🔁 Steps Followed

1. Installed Wireshark on Kali Linux using terminal.
### 1. ✅ Install Wireshark
```bash
sudo apt update
sudo apt install wireshark -y
```
2. Verify the active network interface.
```bash
ifconfig
```
Output showed `eth0` as the active interface.

3. Open Wireshark and begin live capture on `eth0`.
4. Browse websites.
5. Capture data for around 1 minute.
6. Stop the capture and use filters to view specific protocols like `dns`, `tcp`, `http`, and `tls`.
7. Export the capture as a .pcap file.


---

## 📁 Deliverables

- 📄 **Capture File**: [`packet_capture.pcapng`](./packet_capture.pcapng)
- 📄 **Short Report**: Included below

---

## 🔍 Protocols Identified in Capture

| Protocol    | Description                                 | Observation in Capture                                  |
|-------------|---------------------------------------------|---------------------------------------------------------|
| **DNS**     | Domain Name System, resolves hostnames      | Queries made to resolve domains like `google.com`       |
| **ARP**     | Address Resolution Protocol                 | ARP requests to resolve local IPs on the network        |
| **TCP**     | Transmission Control Protocol               | Connection setup with remote servers                    |
| **TLSv1.2** | Encrypted communication over HTTPS          | Secure sessions with Google and W3Schools               |
| **ICMPv6**  | Internet Control Message Protocol (IPv6)    | Multicast and echo request traffic from system          |

---

## 📊 Summary of Findings

- **DNS queries** resolved domain names of the websites visited.
- **TCP traffic** handled the initial handshakes and connections to those domains.
- **TLSv1.2** encrypted the communications, confirming HTTPS usage.
- **ARP packets** show MAC-to-IP resolution activity on the local network.
- **ICMPv6 packets** suggest IPv6 was active and being used for system-level network functions.

These protocols show a healthy and standard network communication pattern when browsing secure websites.

---

## ✅ Conclusion

This task successfully demonstrated:
- Real-time packet capture on Kali Linux
- Interaction of multiple protocols during normal web browsing
- Usage of Wireshark filters to isolate and examine protocol data


---
