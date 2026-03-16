# HP OfficeJet 200 Mobile Printer Deployment & Troubleshooting

## Project Overview

This project documents the deployment, configuration, and troubleshooting of an HP OfficeJet 200 Mobile printer in a Windows environment. The objective was to configure wireless printing using **Wi-Fi Direct and standard Wi-Fi network connectivity**, diagnose hardware issues encountered during setup, and validate successful printing functionality.

This project simulates a **real-world Help Desk / Desktop Support scenario** involving hardware troubleshooting, device configuration, and print validation.

---

# Environment

| Component           | Configuration                     |
| ------------------- | --------------------------------- |
| Printer             | HP OfficeJet 200 Mobile (CZ993A)  |
| Client Device       | Windows Laptop                    |
| Connection Methods  | Wi-Fi Direct / Standard Wi-Fi     |
| Driver Installation | HP Smart / Windows Printer Driver |
| Validation          | Windows Test Page                 |

---

# Skills Demonstrated

* Hardware troubleshooting
* Battery replacement
* Wireless device configuration
* Wi-Fi Direct networking
* Printer driver installation
* Print troubleshooting
* Endpoint device management
* Technical documentation

---

# Network Architecture

### Wi-Fi Direct Mode

Laptop connects directly to the printer without a router.

```
Laptop
   │
   │ Wi-Fi Direct
   │
HP OfficeJet 200
```

### Wi-Fi Network Mode

Printer connects to the local wireless network.

```
Laptop
   │
   │
Wi-Fi Router
   │
   │
HP OfficeJet 200
```

---

# Implementation

## 1. Initial Printer Setup

Steps performed:

1. Powered on printer
2. Installed ink cartridges
3. Verified printer functionality
4. Attempted mobile operation

During this stage a **hardware issue with the battery** was discovered.

---

# Hardware Issue – Battery Failure

## Problem

The printer would only power on when connected to the AC adapter.

### Observed Symptoms

* Printer powered off immediately when unplugged
* Battery indicator showed no charge
* Device functioned normally when connected to AC power

---

## Troubleshooting Steps

Performed the following diagnostics:

1. Verified AC adapter functionality
2. Removed and reseated battery
3. Inspected battery contacts
4. Attempted battery recharge
5. Retested printer without AC power

These steps indicated the battery had failed.

---

## Resolution

The original battery was replaced.

After replacement:

* Battery successfully charged
* Printer powered on without AC adapter
* Mobile functionality restored

---

# Wi-Fi Direct Configuration

Wi-Fi Direct allows devices to connect directly to the printer without requiring a wireless router.

## Steps

1. Navigate to printer **Wireless Settings**
2. Enable **Wi-Fi Direct**
3. Record network information:

```
SSID: DIRECT-xx-HP OfficeJet 200
Password: ********
```

4. On the laptop:

```
Windows Settings
→ Network & Internet
→ Wi-Fi
```

5. Connect to the Wi-Fi Direct network
6. Enter the printer password

Connection was successfully established.

---

# Printer Driver Installation

## Method  – HP Smart

1. Install HP Smart
2. Launch application
3. Select **Add Printer**
4. Printer automatically detected


```

Windows detected and installed the printer driver.

---

# Standard Wi-Fi Network Configuration

The printer was also configured to join the local wireless network.

## Steps

1. Open printer **Wireless Settings**
2. Select **Wireless Setup Wizard**
3. Choose local Wi-Fi network
4. Enter network password
5. Confirm printer successfully joined the network

The printer obtained a network connection and became available to devices on the same network.

---

# Print Issue – Blank Test Page

After installation, the printer accepted print jobs but produced **blank pages**.

## Observed Symptoms

* Paper fed correctly
* Printer completed print job
* Output pages contained no ink

---

## Troubleshooting

Performed the following diagnostics:

1. Verified ink cartridges installed correctly
2. Checked protective tape removal
3. Verified ink levels
4. Ran **Printhead Cleaning**
5. Ran **Printer Alignment**

---

## Resolution

Running the **printhead cleaning cycle** restored ink flow.

---

# Validation

Successful configuration confirmed by:

* Printer powers on using battery
* Laptop connects via Wi-Fi Direct
* Printer joins local Wi-Fi network
* Printer detected by Windows
* Test page prints successfully
* Ink printing correctly

Result:

```
Printer deployment completed successfully.
Wireless printing operational.
```

---

# Screenshots

Recommended screenshots for repository documentation:

```
/screenshots

01_printer_added_windows.png
02_wifi_direct_connection.png
03_wifi_network_connected.png
04_printer_test_page.png
05_battery_replacement.jpg
```

---

# Key Lessons

This deployment demonstrated multiple common Help Desk scenarios:

* Hardware failure diagnosis
* Component replacement
* Wireless device setup
* Driver installation
* Print troubleshooting

These tasks reflect typical **Level 1 / Desktop Support responsibilities**.

---

# Future Improvements

Potential extensions for this project:
* Print spooler troubleshooting
* Network printer deployment via IP


---
