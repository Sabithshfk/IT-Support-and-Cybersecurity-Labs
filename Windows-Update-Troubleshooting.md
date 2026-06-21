# Windows Update Troubleshooting

## Purpose

This guide covers common Windows Update issues and the troubleshooting steps used to resolve them.

---

## Common Symptoms

- Windows Update stuck at 0%, 20%, 50%, or 100%
- Updates fail to install
- Microsoft Store applications fail to download
- Older applications report unsupported Windows version
- Slow system performance due to pending updates

---

## Initial Checks

### Check Internet Connectivity

Verify the PC has a stable internet connection.

```cmd
ping google.com
```

---

### Check Available Disk Space

Ensure sufficient free space is available on the system drive.

Recommended:
- Minimum 20 GB free

---

## Run Windows Update Troubleshooter

1. Open Settings
2. System
3. Troubleshoot
4. Other troubleshooters
5. Windows Update
6. Run

---

## Restart Windows Update Services

Open Command Prompt as Administrator:

```cmd
net stop wuauserv
net stop bits
net stop cryptsvc

net start cryptsvc
net start bits
net start wuauserv
```

---

## Clear Windows Update Cache

Open Command Prompt as Administrator:

```cmd
net stop wuauserv
net stop bits
```

Rename SoftwareDistribution folder:

```cmd
ren C:\Windows\SoftwareDistribution SoftwareDistribution.old
```

Restart services:

```cmd
net start wuauserv
net start bits
```

---

## Repair System Files

### Run SFC

```cmd
sfc /scannow
```

### Run DISM

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

---

## Check Windows Version

Press:

```text
Win + R
```

Type:

```text
winver
```

Verify the system is running a supported Windows version.

Older Windows versions may prevent:
- Microsoft Store downloads
- New applications
- Security updates

---

## Microsoft Store Issues

### Reset Microsoft Store

Press:

```text
Win + R
```

Run:

```cmd
wsreset.exe
```

Wait for the Store to reopen.

---

## Driver Verification

Open:

```text
Device Manager
```

Check for:
- Unknown devices
- Missing drivers
- Network adapter issues

Update drivers where necessary.

---

## Real-World Example

### Customer Issue

- Lenovo 4th Gen i7 desktop
- Very slow performance
- Microsoft game would not download
- Wi-Fi connectivity issues

### Findings

- Windows updates significantly outdated
- Microsoft Store compatibility issues
- Weak Wi-Fi signal due to router placement

### Resolution

- Improved Wi-Fi signal by relocating router
- Started Windows Update process
- Planned remote follow-up using AnyDesk

---

## Prevention

- Keep Windows updated regularly
- Maintain at least 20 GB free disk space
- Update device drivers periodically
- Restart the system after major updates

---

## References

- Microsoft Windows Update
- Microsoft Store Troubleshooting
- SFC and DISM Repair Tools
