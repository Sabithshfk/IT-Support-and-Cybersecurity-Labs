# Windows Performance Optimization

## Purpose

This guide covers methods to improve Windows performance on older and modern computers while maintaining system stability.

---

# Common Symptoms

- Slow startup
- Applications take a long time to open
- High disk usage
- High CPU usage
- Frequent freezing
- Windows Update taking excessive time
- Microsoft Store not functioning correctly
- Slow login

---

# Initial Assessment

Before making changes, check:

- Windows version
- RAM size
- Storage type (HDD or SSD)
- CPU model
- Free disk space

Useful commands:

```cmd
winver
```

```cmd
msinfo32
```

---

# Windows Updates

Install all pending updates.

Settings

Windows Update

Check for Updates

Restart after installation.

---

# Startup Optimization

Open:

Task Manager

Startup Apps

Disable unnecessary startup applications such as:

- Discord
- Steam
- Spotify
- Adobe Updater
- Teams Personal
- OneDrive (if not required)

Do NOT disable:

- Audio drivers
- Touchpad software
- Graphics drivers
- Antivirus

---

# Storage Optimization

Run:

```cmd
cleanmgr
```

Delete:

- Temporary Files
- Windows Update Cleanup
- Recycle Bin
- Delivery Optimization Files

---

# Disk Health

Check drive type.

Settings

System

Storage

If HDD:

- Defragment periodically.

If SSD:

- Never manually defragment.

---

# HDD vs SSD

HDD

Advantages

- Cheaper
- Higher capacity

Disadvantages

- Slow boot
- Slow application loading
- Mechanical failure risk

SSD

Advantages

- Fast boot
- Faster Windows Updates
- Better overall responsiveness
- Silent operation

Recommendation

Upgrade to SSD whenever possible.

---

# Driver Updates

Open:

Device Manager

Check for:

- Unknown devices
- Missing drivers
- Warning icons

Install manufacturer drivers when available.

---

# Windows Repair

Run:

```cmd
sfc /scannow
```

Then:

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

Restart computer afterwards.

---

# Malware Scan

Run Windows Security.

Perform:

- Quick Scan
- Full Scan if required

Remove any detected threats.

---

# Visual Performance

Open:

System

Advanced System Settings

Performance

Settings

Select:

Adjust for best performance

Or manually disable:

- Animations
- Transparency
- Shadows

---

# Browser Optimization

Clear:

- Cache
- Cookies
- Extensions not in use

Update browser to latest version.

---

# Hardware Considerations

Minimum recommended:

- SSD
- 8 GB RAM
- Dual Core or better CPU

For Windows 11:

- SSD
- 16 GB RAM recommended

---

# Real-World Example 1

HP EliteOne 800 G4

Issue

- Audio stopped working after Windows Update.

Resolution

- Rolled back Synaptics audio driver.
- Restarted PC.
- Verified sound functionality before reconnecting to network.

---

# Real-World Example 2

Core 2 Duo Desktop

Specifications

- Core 2 Duo
- 4 GB RAM
- HDD
- Windows 10 22H2

Optimization

- Disabled startup applications.
- Cleaned temporary files.
- Updated Windows.
- Reduced visual effects.

Recommendation

Upgrade HDD to SSD for the greatest improvement.

---

# Real-World Example 3

Lenovo Desktop

Issue

- Very slow performance.
- Microsoft Store applications would not download.

Findings

- Windows significantly outdated.
- Weak WiFi signal.

Resolution

- Recommended moving router.
- Began Windows Update process.
- Planned remote follow-up.

---

# Best Practices

- Keep Windows updated.
- Install official drivers.
- Maintain at least 20 GB free storage.
- Restart computer weekly.
- Avoid unnecessary startup applications.

---

# References

- Microsoft Windows Documentation
- Microsoft Performance Troubleshooting
