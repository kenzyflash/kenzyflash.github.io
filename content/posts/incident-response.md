+++
date = '2026-03-21T10:30:00+03:00'
draft = false
title = 'Incident Response: Ransomware Detection and Containment'
description = 'How to quickly identify and isolate ransomware in an enterprise environment.'
tags = ['incident-response', 'ransomware', 'forensics']
+++

### Overview

This post outlines a rapid incident response flow for suspected ransomware activity in Windows and Linux environments.

### Detection

- Monitor for unusual file I/O spikes
- Alert on renamed files with random extensions
- Identify process anomalies (PowerShell/WMIC in unusual context)

### Containment

1. Disconnect infected hosts from network
2. Isolate remote share mounts
3. Preserve memory/images for forensic analysis

### Remediation

- Restore from verified backups
- Rotate credentials for compromised accounts
- Harden EDR/AV rules and patch related CVEs

### Lessons

- Early detection prevents full domain compromise
- Playbooks + automation are critical for scale
- Keep tabletop exercises current with latest threat patterns
