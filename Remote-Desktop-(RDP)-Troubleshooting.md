# Remote Desktop (RDP) Troubleshooting

## Purpose

This guide explains how to diagnose and resolve common Microsoft Remote Desktop (RDP) connectivity issues in Windows environments.

---

# What is Remote Desktop?

Remote Desktop Protocol (RDP) allows users to remotely connect to and control another Windows computer over a network.

Default RDP Port:

```
3389
```

---

# Common Symptoms

- Unable to connect
- Connection timed out
- Authentication failed
- Black screen after login
- Remote PC not responding
- "Remote Desktop can't connect to the remote computer"

---

# Initial Checks

Before troubleshooting, verify:

- Remote PC is powered on
- Internet/network connection is working
- Correct computer name or IP address
- User has permission to connect

---

# Check Network Connectivity

Ping the remote computer:

```cmd
ping <IP Address>
```

Example:

```cmd
ping 192.168.1.100
```

If ping fails:

- Verify network connectivity
- Check firewall
- Verify IP address

---

# Verify Remote Desktop is Enabled

Settings

↓

System

↓

Remote Desktop

↓

Enable Remote Desktop

---

# Check User Permissions

Open:

System Properties

↓

Remote

↓

Select Users

Ensure the required user account is allowed to connect.

---

# Check Windows Firewall

Allow:

- Remote Desktop

Verify TCP Port:

```
3389
```

is allowed.

---

# Check RDP Service

Open:

```cmd
services.msc
```

Verify:

Remote Desktop Services

Status:

Running

Startup Type:

Automatic

---

# Verify Remote Computer Name

Run:

```cmd
hostname
```

Or:

```cmd
ipconfig
```

Confirm correct details before connecting.

---

# Check Network Profile

Ensure network is:

- Private

instead of

- Public

when appropriate.

---

# Restart RDP Service

Restart:

Remote Desktop Services

if required.

---

# Authentication Problems

If login fails:

Verify:

- Username
- Password
- Domain (if applicable)

Example:

```
COMPUTERNAME\User
```

or

```
DOMAIN\User
```

---

# Black Screen After Login

Possible causes:

- Graphics driver issue
- Slow network
- Explorer.exe failed to load

Possible fixes:

- Disconnect and reconnect
- Restart Explorer
- Update graphics driver

---

# Command Line Tools

Check IP:

```cmd
ipconfig
```

Check hostname:

```cmd
hostname
```

Check network:

```cmd
ping <IP>
```

---

# Common Causes

- Firewall blocking RDP
- Incorrect IP
- Wrong credentials
- RDP disabled
- Remote PC asleep
- VPN disconnected
- DNS resolution issues

---

# Preventive Maintenance

- Keep Windows updated
- Use strong passwords
- Enable MFA where available
- Document IP addresses
- Verify backups before major changes

---

# Real-World Example

Scenario:

Provided remote IT support using AnyDesk for a customer's Windows computer.

Issue:

- Computer was outdated.
- Microsoft Store applications failed.
- Performance was poor.

Actions:

- Planned Windows updates remotely.
- Performed software troubleshooting.
- Restored network connectivity after improving WiFi signal.

Outcome:

Remote support reduced the need for another on-site visit and allowed troubleshooting to continue efficiently.

---

# References

- Microsoft Remote Desktop Documentation
- Microsoft Windows Networking Documentation
