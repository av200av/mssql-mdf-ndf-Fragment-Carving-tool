# mssql-mdf-ndf-Fragment-Carving-tool
Read-only SQL Server fragment carving tool. Recover lost MDF/NDF files by carving scattered SQL Server data pages from disk partitions or disk images, supports SQL Server 2005~2025.
# MSSQL MDF/NDF Fragment Carving Tool
A read-only SQL Server fragment carving utility, built specifically for **lost or deleted MDF/NDF database files**.

## Overview
This tool performs offline, read-only analysis on raw disk partitions and disk image files.
It scans raw disk space to locate scattered SQL Server data pages, extracts these fragments, and reassembles them to reconstruct complete MDF / NDF database files, when the original MDF/NDF files are lost, deleted or unrecoverable via normal file system methods.

This tool works at raw disk / disk image level, dedicated to reconstructing lost primary and secondary SQL Server database files.
All scanning operations run in **read-only mode**. Your source disk partitions and disk images will never be modified.

## Supported Versions
- SQL Server 2005 ~ SQL Server 2025

## Core Capabilities
- Carve SQL Server data pages from raw disk partitions
- Carve SQL Server data pages from disk image files (DD, E01, VMDK, VHD and more)
- Extract scattered database page fragments
- Reassemble fragments to rebuild complete MDF and NDF database files
- Preview extracted page structures before export
- **100% read-only scan**: source disk and image files remain untouched

## Use Cases
- MDF / NDF files are permanently deleted and cannot be restored from recycle bin
- File system metadata is damaged, original MDF/NDF files are lost
- Disk formatted, database files erased, but raw data pages still exist on disk
- Forensic recovery of lost SQL Server primary/secondary database files from disk clones

## How It Works
1. The tool scans disk partition or disk image in read-only mode.
2. It identifies SQL Server data page signatures from raw unallocated disk space.
3. Collects and sorts scattered MDF/NDF page fragments.
4. Reassembles fragments to reconstruct intact MDF / NDF files.
5. Preview the recovered database structure before export.

## Important Notice
This is an offline forensic analysis tool.
We do **not** write or modify the original disk partitions or disk image files during scanning. Always work on disk copies or disk images for evidence safety.

## Download
Get the latest Windows binary release on GitHub Releases.

> Pre-built Windows x64 zip package, contains the read-only MSSQL MDF/NDF fragment carving client.

## Antivirus Note
> ⚠️ The Windows binary is protected with VMProtect for anti-tampering. Some antivirus software may incorrectly flag it as malware (false positive). This tool works in fully read-only mode and will not modify your disk or image files.

## Contact
For technical feedback, bug reports or feature requests, please open a GitHub issue.
