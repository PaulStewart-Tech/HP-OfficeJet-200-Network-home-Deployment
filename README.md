# 🖨 Network Printer Deployment & Troubleshooting

## HP OfficeJet 200 Mobile (CZ993A)

## 📌 Project Overview

Deployed and configured a portable wireless printer — **HP OfficeJet 200 Mobile (CZ993A)** — in a Windows 10 lab environment.

This project simulates a real-world Help Desk ticket involving:

* Wireless printer deployment
* Driver installation & validation
* TCP/IP manual printer configuration
* DHCP IP changes causing “Printer Offline”
* Wi-Fi Direct vs Infrastructure mode comparison
* Root cause analysis and resolution

The objective was to document structured troubleshooting methodology consistent with Level 1 IT Support practices.

---

## 🖥 Lab Environment

| Component     | Configuration                                |
| ------------- | -------------------------------------------- |
| Client OS     | Windows 10 Pro                               |
| Network       | DHCP-enabled home lab router                 |
| Printer       | HP OfficeJet 200 Mobile                      |
| Connectivity  | Wi-Fi Infrastructure Mode                    |
| Power         | Battery-operated (tested unplugged scenario) |
| IP Assignment | DHCP → DHCP Reservation                      |

---

## 🎯 Deployment Objectives

1. Connect printer to wireless infrastructure network
2. Verify assigned IP address
3. Validate connectivity from client system
4. Install manufacturer driver package
5. Add printer manually via TCP/IP
6. Simulate offline scenario and resolve

---

# 🔧 Phase 1 – Wireless Network Configuration

Connected printer to lab Wi-Fi via onboard display.

Retrieved assigned IP address from:

* Printer network configuration page

Validated connectivity:

```
ping <printer-ip>
```

✔ Successful ICMP response confirmed network layer communication.

---

# 🧩 Phase 2 – Driver Installation & Validation

Installed official HP driver package to ensure:

* Full feature access
* Status monitoring
* Proper spooler integration

Compared:

* Windows automatic driver install
* HP full driver package

Final implementation: HP driver for stability and complete functionality.

Tested:

* Print queue visibility
* Test page print
* Printer status reporting

---

# 🌐 Phase 3 – Manual TCP/IP Printer Addition

Simulated enterprise deployment method:

1. Control Panel → Devices & Printers
2. “The printer I want isn’t listed”
3. Add printer using TCP/IP address
4. Created Standard TCP/IP port
5. Entered printer IP manually

✔ Successful manual configuration.

Reasoning:

In enterprise environments:

* Broadcast discovery may be disabled
* Printers are deployed via IP or print server
* Manual port configuration is common

---
⚠ Incident: Printer Powers Off When Unplugged
Symptoms

Device boots normally on AC power

Shuts down immediately when AC removed

Battery indicator does not retain charge

Investigation

Verified AC adapter voltage output stable

Confirmed device stable while plugged in

Observed no charge retention over extended period

Isolated battery as single failure domain

Root Cause

Degraded internal lithium-ion battery.

**Resolution Options**

*Replace battery pack
*Operate in AC-only mode
*Evaluate cost vs replacement printer

# ⚠ Simulated Incident: Printer Showing “Offline”

## Scenario

After router reboot:

* Printer received new DHCP IP
* Windows printer port still pointed to old IP
* Status showed “Offline”

---

## Investigation Steps

* `ping <old-ip>` → Failed
* Printed new network config page
* Verified new DHCP-assigned IP
* Confirmed mismatch in printer port settings

---

## Root Cause

Dynamic IP reassignment caused TCP/IP port misconfiguration.

---

## Resolution

Implemented DHCP reservation on router to bind printer MAC address to fixed IP.

Updated printer port configuration to new reserved IP.

---

## Validation

* Successful ping response
* Test page printed successfully
* Status returned to “Ready”

---

# 🔎 Additional Testing

### Wi-Fi Direct Mode

Tested direct connection mode:

* Connected laptop directly to printer SSID
* Printed test document
* Observed limited network accessibility

Conclusion:

Wi-Fi Direct useful for field/mobile deployment but not ideal for structured network environments.

---

# 🧠 Skills Demonstrated

* Network troubleshooting
* ICMP validation
* DHCP understanding
* IP reservation configuration
* TCP/IP printer deployment
* Windows spooler validation
* Root cause analysis
* Structured incident documentation

---

# 📂 Repository Structure

```
HP-OfficeJet-200-Deployment/
│
├── README.md
├── screenshots/
│   ├── network-config-page.png
│   ├── ping-test.png
│   ├── tcp-ip-port-settings.png
│   ├── driver-install.png
│   ├── offline-error.png
│   └── test-print-success.png
└── incident-report.md
```


* Create a Jira-style ticket summary for this
* Or review it brutally and tell you if it’s strong enough for Toronto entry-level IT roles

Your move.
