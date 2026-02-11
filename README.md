# network-troubleshooting-lab
# Technical Support Troubleshooting Report
**Author:** Thandeka Mbokazi
**Date:** February 11, 2026

## 1. System Information & Network Status
The following specifications were gathered from the personal desktop settings and command line:

* **Network Adapter:** Intel(R) Dual Band Wireless-AC 3165
* **Connection Type:** Wi-Fi 5 (802.11ac)
* **IP Address:** 192.168.1.10

![System Network Properties](err2.png)

---

## 2. Issue Description
The system was unable to connect to the internet. While the Wi-Fi icon indicated a connection to the SSID "CapaCiTi Candidates 5GHz," no web traffic could be sent or received.

### Initial Verification
I attempted to ping Google to check connectivity. The request failed immediately, indicating a name resolution or connectivity issue.

![Failed Ping Test](Err1.png)

---

## 3. Troubleshooting & Diagnosis
I ran `ipconfig /all` to inspect the network configuration. I discovered that **DHCP (Dynamic Host Configuration Protocol)** was disabled for the Wi-Fi adapter. Without DHCP, the system was not receiving correct DNS server information from the router.

![IP Config Diagnosis](err3.png)

---

## 4. Resolution
I utilized the **Windows Network Diagnostics** tool to reset the adapter settings. The tool automatically identified that DHCP was disabled and re-enabled it.

![Resolution via Windows Troubleshooter](Err5.png)

**Final Verification:** After the troubleshooter finished, I successfully flushed the DNS and verified that internet access was restored.
