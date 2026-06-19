# DHCP Basics and Troubleshooting

## What is DHCP?

DHCP (Dynamic Host Configuration Protocol) automatically assigns IP addresses and network settings to devices.

Without DHCP, IP addresses would need to be configured manually.

---

## Information Provided by DHCP

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

---

## Common DHCP Problems

- Device receives no IP address
- IP address conflict
- Unable to access network
- DHCP server unavailable

---

## Troubleshooting Steps

### 1. Check IP Address

Run:

ipconfig

Verify whether the device has:
- Valid IP address
- APIPA address (169.254.x.x)

### 2. Renew IP Address

Run:

ipconfig /release

ipconfig /renew

### 3. Check Physical Connection

Verify:
- Ethernet cable
- Switch port
- Wi-Fi connection

### 4. Verify DHCP Server

Ensure DHCP server is online and functioning.

### 5. Restart Network Adapter

Disable and enable the adapter.

---

## Interview Question

### What is DHCP?

DHCP automatically assigns IP addresses and network settings to devices on a network.

### What happens if DHCP fails?

The device may not receive a valid IP address and may be unable to communicate on the network.
