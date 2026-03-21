+++
date = '2026-03-21T09:00:00+03:00'
draft = false
title = 'CTF Web Exploitation Writeup'
description = 'A step-by-step deconstruction of a recent web vulnerability challenge.'
tags = ['ctf', 'web', 'security']
+++

## Challenge: `headless-web`

This writeup covers exploitation of a vulnerable web application deployed as a CTF challenge. The test setup included:

- insecure file upload
- weak session management
- arbitrary command injection

### 1. Recon

Start by exploring endpoints and validating behavior under authenticated and unauthenticated sessions.

### 2. Exploitation

Found insecure file upload endpoint `/upload` without mime or extension filtering.

Uploaded PHP webshell and gained remote command execution.

### 3. Fix

- validate file type and extensions strictly
- enforce strong session cookie attributes (`HttpOnly`, `Secure`)
- apply Web Application Firewall rules for command injection


## Post-mortem

This demonstrates how configuration issues in common web stacks can lead to path traversal and RCE.
