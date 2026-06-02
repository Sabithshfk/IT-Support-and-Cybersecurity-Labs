# PXE Boot Error Troubleshooting

## What is PXE?

PXE (Preboot Execution Environment) allows a computer to boot from a network server instead of a local disk.

## Common Causes

- HDD/SSD not detected
- Wrong boot order
- OS corruption
- Failed storage device
- Missing bootloader

## Troubleshooting Steps

1. Check BIOS detects SSD/HDD
2. Verify boot order
3. Check SATA/NVMe settings
4. Run hardware diagnostics
5. Repair OS boot files
6. Reinstall OS if required

## Interview Answer

A PXE error usually indicates that the system cannot find a bootable operating system and is attempting network boot. I would first verify that the storage device is detected and then check the boot order before investigating OS corruption or hardware failure.
